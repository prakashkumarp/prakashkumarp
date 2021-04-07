# Driver Drowsiness Detection
- **Modules**
-1. **FacialLandmarks**

      import the necessary packages for facial landmarks detection
       from imutils import face_utils
       import dlib
       import cv2
 

       p = "shape_predictor_68_face_landmarks.dat"
       detector = dlib.get_frontal_face_detector()
      predictor = dlib.shape_predictor(p)

      cap = cv2.VideoCapture( 0,cv2.CAP_DSHOW)
 
      while True:
     load the given image and convert it into grayscale
     _, image = cap.read()
      gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
        
    detecting face in the grayscale image
    rects = detector(gray, 0)
    
    looping over the face detections
    for (ind, rect) in enumerate(rects):
         determine the facial landmarks for the face region, then
         convert the facial landmark (x, y)-coordinates to a NumPy
         array
        shape = predictor(gray, rect)
        shape = face_utils.shape_to_np(shape)
    
         loop over the (x, y)-coordinates for the facial landmarks
         drawing the marks on the image
        for (x, y) in shape:
            cv2.circle(image, (x, y), 1, (0, 255, 0), 2)
    
   
    cv2.imshow("Output", image)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

     cv2.destroyAllWindows()
     cap.release()


-2. **Yawing**
 
      import cv2
     import dlib
     import numpy as np
      PREDICTOR_PATH = "shape_predictor_68_face_landmarks.dat"
     predictor = dlib.shape_predictor(PREDICTOR_PATH)
      #cascade_path='haarcascade_frontalface_default.xml'
     #cascade = cv2.CascadeClassifier(cascade_path)
     detector = dlib.get_frontal_face_detector()


    def get_landmarks(im):
    rects = detector(im, 1)

    if len(rects) > 1:
        return "Error"
    if len(rects) == 0:
        return "Error"
    return np.matrix([[p.x, p.y] for p in predictor(im, rects[0]).parts()])

 
    def anno_landmarks(im, landmarks):
    im = im.copy()
    for ind, point in enumerate(landmarks):
        pos = (point[0, 0], point[0, 1])
        cv2.putText(im, str(ind), pos,
                    fontFace=cv2.FONT_HERSHEY_SCRIPT_SIMPLEX,
                    fontScale=0.4,
                    color=(0, 0, 255))
        cv2.circle(im, pos, 3, color=(0, 255, 255))
    return im

    def top_lip(landmarks):
    top_lip_pnts = []
    for i in range(50,53):
        top_lip_pnts.append(landmarks[i])
    for i in range(61,64):
        top_lip_pnts.append(landmarks[i])
    top_lip_all_pts = np.squeeze(np.asarray(top_lip_pnts))
    top_lip_mean_is = np.mean(top_lip_pnts, axis=0)
    return int(top_lip_mean_is[:,1])

     def bottom_lip(landmarks):
    bottom_lip_pts = []
    for i in range(65,68):
        bottom_lip_pts.append(landmarks[i])
    for i in range(56,59):
        bottom_lip_pts.append(landmarks[i])
    bottom_lip_all_pts = np.squeeze(np.asarray(bottom_lip_pts))
    bottom_lip_mean = np.mean(bottom_lip_pts, axis=0)
    return int(bottom_lip_mean[:,1])

     def is_mouth_open(image):
    landmarks = get_landmarks(image)
    
    if landmarks == "error":
        return image, 0
    
    image_with_landmarks = anno_landmarks(image, landmarks)
    top_lip_center = top_lip(landmarks)
    bottom_lip_center = bottom_lip(landmarks)
    lip_distance = abs(top_lip_center - bottom_lip_center)
    return image_with_landmarks, lip_distance

    #cv2.imshow('Result', image_with_landmarks)
    #cv2.imwrite('image_with_landmarks.jpg',image_with_landmarks)
    #cv2.waitKey(0)
    #cv2.destroyAllWindows()

     cap = cv2.VideoCapture(0)
     yawns = 0
    yawn_statu = False 

     while True:
    ret, frame = cap.read()   
    image_landmarks, lip_distance = is_mouth_open(frame)
    
    prev_yawn_status = yawn_statu  
    
    if lip_distance > 20:
        yawn_statu = True 
        
        cv2.putText(frame, "You are Yawning", (50,450), 
                    cv2.FONT_HERSHEY_COMPLEX, 1,(0,0,255),2)
        

        output_text = " YawnCount: " + str(yawns + 1)

        cv2.putText(frame, output_text, (50,50),
                    cv2.FONT_HERSHEY_COMPLEX, 1,(0,255,127),2)
        
    else:
        yawn_statu = False 
         
    if prev_yawn_status == True and yawn_statu == False:
        yawns += 1

    cv2.imshow('Live Landmarks', image_landmarks )
    cv2.imshow('Yawn Detection', frame )
    
    if cv2.waitKey(1) == 13: #13 is the Enter Key
        break
        
       cap.release()
    cv2.destroyAllWindows() 
