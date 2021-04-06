- 👋 Hi, I’m @prakashkumarp
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- why is this happening to me oh man


RESEARCH PAPER 
 - **ABSTRACT**:
Driver fatigue is one of the major issue causes accidents in the world. Detecting the driver drowsiness is one  of  the  solution  for  the above problem. In this project we aim to detect drowsiness of the driver using    opencv   by  monitoring the eyes of the driver. If the eyes closed certain time period  than  the alarm sound alert the driver. In addition to the above problem in this project we detect the face of the driver, age of the driver and gender of the driver using opencv and machine learning algorithms.
KEYWORDS: Driver drowsiness, eye detection, opencv.

- **INTRODUCTION**: 
In the world every day  a lot of accidents are happening because of driver fatigue. Vehicles are increasing rapidly. A  lot of new vehicles launching every day in the world. In these vehicles speed limit is extremely high, they are very fast. So drivers has to be very careful while driving these high speed vehicles on the road. In lot of cities the roads are not good up to the speed of the new vehicles. So  a lot of accidents happening on the roads. It has a lot of effect on our  life. One of the major issue is driver fatigue. Because of driver fatigue daily  a lot of accidents happening in the world. It  effects a lot in the world. Educated people or non educated people are seriously effecting these road accidents because of driver fatigue. So driver fatigue is the major issue in the world. One of the solution to driver fatigue is detecting driver drowsiness. For this problem we can find solution using machine learning. Machine learning has lot of techniques and algorithms for this problem. One of the technique is OpenCV (open source computer vision). OpenCV has inbuilt algorithm to capture the image from the web cam. We use OpenCV technique for detecting images from the camera, edit the images, write something on the detected images, crop images on the detected images, copy images. After  detecting image through OpenCV we can find the age of the driver, gender of the driver, face of  the driver. For detecting age, gender,face of a driver we use CNN(Convolutional neural network) algorithm.

- **EXISTING SYSTEM**:
Gaussian Mixture Models was used to represent the distribution of facial patches. In GMM were used again for representing the distribution of local facial  measurements, but robust descriptors were used instead of pixel patches. Finally, instead of GMM ,Hidden-MarkovModel, super-vectors were used for representing face patch distributions.  SVM classifiers were used by, applied directly to image insensities. Rather than using SVM, used Adaboost for the same purpose, here again applied to image intensities. Finally,viewpoint-invariant age and gender classification was presented.
- Disadvantages:
-A drawback of those methods is that they require input images to be near-frontal and well-aligned. These methods therefore present experimental results only on constrained data sets of near-frontal images.

- **SOFTWARE REQUIREMENT SPECIFICATION**

- 5.1 Requirements Specification: 

Requirement Specification provides a high secure storage to the web server efficiently. Software requirements deal with software and hardware resources that need to be installed on a serve which provides optimal functioning for the application. These software and hardware requirements need to be installed before the packages are installed. These are the most common set of requirements defined by any operation system. These software and hardware requirements provide a compatible support to the operation system in developing an application.

- 5.1.1 **HARDWARE REQUIREMENTS**: 
The hardware requirement specifies each interface of the software elements and the hardware elements of the system. These hardware requirements include configuration characteristics.
System		 : Pentium IV 2.4 GHz. 
Hard Disk 	 : 320 GB. 
Monitor	 : 15 VGA Color. 
Mouse		 : Logitech. 
RAM		 : 4 GB. 

- 5.1.2 **SOFTWARE REQUIREMENTS**:
The software requirements specify the use of all required software products like data management system. The required software product specifies the numbers and version. Each interface specifies the purpose of the interfacing software as related to this software product.
Operating system 	: 	Windows XP/7/10
Coding Language	: 	python
Library     	          :             opencv
IDE 			: 	PYCHARM

- **PROPOSED SYSTEM**:
In this project we aim to detect drowsiness of the driver using    opencv   by  monitoring the eyes of the driver. If the eyes closed certain time period  than  the alarm sound alert the driver. In addition to the above problem in this project we detect the face of the driver, age of the driver and gender of the driver using opencv and machine learning algorithms.
ADVANTAGES:
1.Easy to execute effective than other approaches.
2.Easy to create and learn.
3.Gives high accuracy than previous ones.
- LITERATURE SURVEY:
Age and Gender Classification Age classification. The problem of automatically extracting age related attributes from facial images has received increasing attention in recent years and many methods have been put fourth. A detailed survey of such methods can be found in  and, more recently, in . We note that despite our focus here on age group classification rather thanprecise age estimation (i.e., age regression), the survey below includes methods designed for either task. Early methods for age estimation are based on calculating ratios between different measurements of facial features. Once facial features (e.g. eyes, nose, mouth, chin, etc.) are localized and their sizes and distances measured, ratios between them are calculated and used for classifyingthe face into different age categories according to hand-crafted rules. More recently, uses a similar approach to model age progression in subjects under 18 years old. As those methods require accurate localization of facial features, a challenging problem by itself, they are unsuitablefor in-the-wild images which one may expect to find on social platforms. On a different line of work are methods that represent the aging process as a subspace  or a manifold . A drawback of those methods is that they require input images to be near-frontal and well-aligned. These methods therefore present experimental results only on constrained data-sets of near-frontal images. Again, as a consequence, such methods are ill-suited for unconstrained images.  Different from those described above are methods that use local features for representing face images. In  Gaussian Mixture Models (GMM)  were used to represent the distribution of facial patches. In  GMM were used again for representing the distribution of local facial measurements, but robust descriptors were used instead of pixel patches. Finally, instead of GMM, Hidden-Markov-Model, super-vectors were used in  for representing face patch distributions. An alternative to the local image intensity patches are robust image descriptors: Gabor image descriptors  were used in  along with a Fuzzy-LDA classifier which considers a face image as belonging to more than one age class. In  a combination of Biologically-Inspired Features (BIF)  and various manifold-learning methods were used for age estimation. Gabor and local binary patterns (LBP)  features were used in  along with a hierarchical age classifier composed of Support Vector Machines (SVM)  to classify the input image to an age-class. followed by a support vector regression  to estimate a precise age. Finally, proposed improved versions of relevant component analysis  and locally preserving projections . Those methods are used for distance learning and dimensionality reduction, respectively, with Active Appearance Models as an image feature. All of these methods have proven effective on small and/or constrained benchmarks for age estimation. To our knowledge, the best performing methods were demonstrated on the Group Photos benchmark .In  state-of-the-art performance on this benchmark was presented by employing LBP descriptor variations  and a dropout-SVM classifier. We show our proposed method to outperform the results they report on the more challenging Audience benchmark, designed for the same task.  Gender classification. A detailed survey of gender classification methods can be found in and more recently n . Here we quickly survey relevant methods. One of the early methods for gender classification used a neural network trained on a small set of near-frontal face images. In  te combined 3D structure of the head (obtained using a laser scanner) and image intensities were used for classifying gender. SVM classifiers were used by , applied directly to image intensities. Rather than using SVM, usedAdaBoost for the same purpose, here again, applied to image intensities. Finally, viewpoint-invariant age and gender classification was presented by .More recently,  used the Webers Local texture Descriptor for gender recognition, demonstrating near perfect performance on the FERET benchmark . In , intensity, shape and texture features were used with mutual information, again obtaining near-perfect results onthe FERET benchmark.
SYSTEM DESIGN:

- **Modules**:
 - Detecting driver face:

This is the system's initialization level. The device must be set up and configured for the current user and conditions every time it is started. The effective identification of heads is the most important step in this level (Figure 2). We can now remove the driver's head if it has been correctly found. The following are the steps in the setup process: I extracting the driver's skin colour and using that information to create a custom skin colour model; and (ii) collecting open/closed eye samples as well as the driver's usual head position. User engagement may be necessary to help achieve these objectives. The driver may be asked to sit comfortably in his or her usual driving position so that the device can assess the upper and lower thresholds required to detect possible nodding. The driver may even be asked to shut their eyes for a few seconds before opening them again. This is sufficient to get the machine up and running. The system's dataset of obtained images will develop over time, and it will be improved.
- Tracking  :
The device enters the normal tracking (monitoring) stage once the driver's head and eyes have been properly identified and all appropriate features have been removed. The continuous monitoring of the driver's eyes within a dynamically allocated tracking area is a key phase in this level. More precisely, the device can assess the size of the monitoring area based on the past history of eye movements to save processing time. For example, if the eyes have been shifting horizontally to the left for a number of frames, that trend is likely to continue in the next frame. As a result, it makes sense to extend the tracking region in the predicted direction of the eyes while shrinking it in the other three directions. The device must also decide the state of the eyes at this stage. Both of these tasks must be completed in real time; depending on the processor's capabilities and current load, it may be possible to skip a few frames from time to time without compromising algorithmic efficiency.
- Warning to the driver:
 The driver's alertness must be boosted if he holds his eyes closed for an extended period of time or begins to nod. The main move in this stage is to keep a close eye on the driver's eyes. The machine must figure out whether the eyes are still closed and where they are in relation to previously defined thresholds. At this point, we can't afford to miss frames.  In practise, eye tracking is done in much the same way as the tracking point, with the addition of the following processes: eye velocity and trajectory measurement, and threshold monitoring. These extra calculations are needed to boost the system's ability to decide whether or not the driver is drowsy.

- Alertness :
Once the machine has established that the driver appears to be in an irregular driving condition, it must be vigilant in alerting the driver of possible dangers. To draw the driver's attention and increase their alertness level, a combination of audio/visual warnings are used. Alerting has to be implemented in such a way as not to cause the opposite effect of intended and startle the driver into causing an accident.

Load Dataset or gathering data:
The quantity & quality of your data dictate how accurate our model is
The outcome of this step is generally a representation of data which we will use for training
Load data set using pandas read_csv() method.

- Split Data Set:
Wrangle data and prepare it for training
Clean that which may require it (remove duplicates, correct errors, deal with missing values, normalization, data type conversions, etc.)
Randomize data, which erases the effects of the particular order in which we collected and/or otherwise prepared our data
Visualize data to help detect relevant relationships between variables or class imbalances (bias alert!), or perform other exploratory analysis
Split into training and evaluation sets
Split the data set to two types. One is train data test and another one is test data set.

- Train data set:

At the heart of the machine learning process is the training of the model. Bulk of the “learning” is done at this stage.
Train data set will train our data set using fit method.

- Test data set:
Test data set will test the data set using algorithm.

- Predict data set:
Predict() method will predict the results.



- RESULTS AND CONCLUSIONS:
The developed drowsiness detection and correction system is capable of detecting drowsiness quickly. The machine can distinguish between natural eye twitch and drowsiness, preventing the driver from falling asleep behind the wheel. The machine works well even when drivers are wearing glasses and in low-light situations. The machine will determine if the eyes are open or closed during the monitoring. The alarm beeps to warn the driver when the eyes are closed for about two seconds. Many incidents can be avoided as a result of this, as well as the driver's and vehicle's protection. Only the most expensive cars have a system for driver protection and vehicle security. Driver protection can be introduced in standard cars using a drowsiness warning system
COMPARATIVE ANALYSIS OF DROWSINESS DETECTION TECHNIQUE:

method	metric	classifier	accuracy
Vehicle-based features	Steering wheel movement (SWM) Standard deviation of lane position (SDLP)	Multi-level back propagation neural network	88.02%
Physiological and behavioral features	ECG, EEG, Pulse rate	Support Vector Mechanism (SVM), Karolinska sleepiness scale (KSS)	80%

.
- CONCLUSION:
The proposed one is successfully run and tested. It is detecting accurately driver drowsiness and age, gender, face of a driver. The proposed algorithm for detecting face,gender,age is cnn. For detecting drowsiness we use OpenCV technique.

- SCOPE FOR FUTURE WORK: 
Future research can concentrate on the use of external factors for fatigue calculation, such as vehicle states, sleeping hours, weather conditions, mechanical details, and so on. Driver drowsiness is a major threat to highway safety, and it is particularly problematic for commercial motor vehicle operators. This severe safety problem is exacerbated by 24-hour activities, high annual mileage, exposure to hazardous environmental conditions, and demanding work schedules. One key step in a series of preventive steps required to solve this issue is to monitor the driver's state of drowsiness and vigilance and provide feedback on their condition so that they can take appropriate action. Currently, there is no way to change the camera's zoom or direction when it is in use. It's likely that future studies will involve automatically zooming in on the eyes once they've been found.
REFERENCES:[1] COMPUTATIONALLY EFFICIENT FACE DETECTION; B. 
SCHLKOPF-A. BLAKE, S. ROMDHANI, AND P. TORR. 
 
[2] USE OF THE HOUGH TRANSFORMATION TO DETECT LINES AND 
CURVES IN PICTURE; R. DUDA AND P. E. HART. 
 
[3] JAIN, “FACE DETECTION IN COLOR IMAGES; R. L. HSU, M. ABDEL-
MOTTALEB, AND A. K. JAIN. 
 
[4] OPEN/CLOSED EYE ANALYSIS  FOR DROWSINESS DETECTION; 
P.R. TABRIZI AND R. A. ZOROOFI. 
 
[5] http://ncrb.gov.in/StatPublications/ADSI/ADSI2015/chapter1A%20traffic
%20accidents.pdf 
 
[6] http://www.jotr.in/text.asp?2013/6/1/1/118718 
 
[7] http://dlib.net/face_landmark_detection_ex.cpp.html

<!---
prakashkumarp/prakashkumarp is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
