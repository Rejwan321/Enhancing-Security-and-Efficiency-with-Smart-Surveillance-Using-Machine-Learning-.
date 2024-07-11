                                                                              Enhancing Security and Efficiency with Smart Surveillance Using Machine Learning
                                                                            -------------------------------------------------------------------------------------
                                                                             Department of Computer Science and Engineering, Narula Institute of Technology,
                                                                             81, Nilgunj Road, Agarpara, Kolkata - 700109, West Bengal


                                                                                                          Abstract
													-------------  
The proposed system offers an innovative solution to address crowd control, security, and worker tracking challenges using Artificial Intelligence and Machine Learning. Specifically designed to support the Indian Railways and relevant authorities, the system aims to enhance operational efficiency and security. Its core functionality focuses on advanced crowd management through ML algorithms, instantly alerting authorities when predefined thresholds are exceeded. The system also utilises AI to detect potentially violent actions and suspicious activities, providing real-time insights through a user-friendly dashboard for 24/7 monitoring. With versatility in resource allocation and scalability in densely populated areas, the system's cloud-based infrastructure ensures ease of integration, cost efficiency, and adaptability. However, success depends on high-quality video feeds, stable internet connectivity, user-friendliness, and seamless integration with existing CCTV systems. In conclusion, this AI and ML-based system offers a comprehensive, real-time solution for security enhancement and efficiency across public and private sectors.

                                                                                                       Introduction
												     ----------------

[1]Enhancing security and operational efficiency has become a pivotal goal across various sectors, especially in environments like transportation hubs, where ensuring safety amidst high traffic volumes is paramount. [1]Smart surveillance systems, empowered by machine learning algorithms, have emerged as game-changers in revolutionising traditional security measures.[1]This amalgamation offers a proactive approach to monitoring, enabling the identification of potential threats in real time while optimising resource allocation and operational workflows.
For instance, in rail stations, the integration of machine learning into surveillance cameras presents a transformative shift. These advanced systems possess the ability to intellect patterns of behaviour, distinguishing between routine commuter activities and suspicious or inconsistent actions. By leveraging predictive analytics and pattern recognition, these smart cameras enhance threat detection capabilities, offering security personnel timely alerts to address security concerns swiftly.

Moreover, the adaptive nature of machine learning in surveillance enables continuous improvement. These systems learn from historical data, evolving their algorithms to better adapt to the dynamic environment of rail stations. The HOG descriptor[10,11] focuses on the structure or the shape of an object. It is better than any edge descriptor as it uses magnitude as well as the angle of the gradient to compute the features. For the regions of the image, it generates histograms using the magnitude and orientations of the gradient. As a result, false alarms decrease, allowing security teams to focus their attention on genuine threats, thereby optimising resource utilisation.

[2] In essence, the convergence of machine learning and smart surveillance technologies in rail station security marks a significant leap forward. This synergy not only fortifies security protocols but also streamlines operations, fostering a safer and more efficient environment for commuters and staff alike.

[5] For example, at a busy rail station, smart surveillance utilising machine learning transforms security. Cameras equipped with AI algorithms swiftly detect anomalies, differentiating between routine activity and potential threats like unattended luggage. [5]These systems continuously learn from station patterns, reducing false alarms and enhancing threat recognition. [5]This proactive approach ensures a safer environment while optimizing operations, allowing security personnel to focus on genuine risks. Ultimately, passengers benefit from heightened security measures and smoother travel experiences.
In these given examples we are using the algorithm [5]YOLOv3 for real-time object detection and AlphaPose for checking the movement and poses of the human body. YOLOv3 
We are also using CNN and computer vision.

[1] CNN stands for Convolution neural network. Their primary function revolves around analysing visual data captured by surveillance cameras.[1]CNNs can detect unusual activities within the monitored area, signalling security teams to potential security risks.[1]CNNs process visual data in real time, enabling immediate analysis and response to security concerns. This paper implements automatic gun (or) weapon detection using a convolution neural network (CNN) based SSD and Faster RCNN algorithms.

[7] Computer vision helps make surveillance smarter and more effective using machines that learn Imagine the security cameras at a train station—computer vision lets these cameras understand what they see. [7]They're trained to spot unusual things, like a bag left alone for a long time or someone acting strangely. With computer vision, these cameras can quickly tell if something isn’t right and alert security. 

Posture tracking is a deep learning process where the algorithm tracks the movement of an object. Posture-tracking algorithms monitor and analyse human body positions and movements. They differentiate between normal and abnormal activities or unusual activities. By continuously tracking and analysing body postures, these systems detect suspicious activities such as individuals loitering in restricted areas, acting aggressively, etc. 

In contemporary rail station security, the imperative to ensure passenger safety and operational efficiency is met with challenges in swiftly identifying potential threats or unusual activities within vast and busy environments. Traditional surveillance systems often struggle to provide real-time insights, leading to delays in threat detection and resource allocation. While existing research has explored various deep learning algorithms, such as SSD and Faster R-CNN, for weapon detection, centralised crime management systems, and real-time incident captioning, there remains a need for an integrated approach that combines advanced machine learning techniques to address the limitations and gaps observed in current methodologies.

The primary challenges include the tradeoff between speed and accuracy in weapon detection, the lack of explicit algorithms mentioned in centralised crime management systems, and the need for more precise human action detection in crowded environments. Furthermore, existing methodologies may not fully leverage posture tracking for comprehensive human activity analysis. There is also a notable gap in addressing the limitations of current research, highlighting the need for an improved, adaptive, and efficient surveillance system in rail stations.

Hence, the problem at hand is to enhance rail station security by developing a comprehensive and integrated surveillance system that employs advanced machine learning algorithms for posture tracking, human action detection, and activity captioning. This system aims to overcome the limitations of existing methodologies, providing a more accurate and efficient means of identifying potential threats, distinguishing between routine and abnormal activities, and ensuring real-time alerts for immediate intervention by security personnel. The goal is to create a holistic solution that optimises resource utilisation, minimises false alarms, and fosters a safer and more efficient travel experience for all commuters in rail stations.

                                                                                                           1. Literature survey :
                                                                                                        ----------------------------
Multiple research works were studied and their findings are summarised in this section. Authors of [1] propose methods to detect weapons from the given images. It uses deep learning algorithms like Single Shot Detector (SSD) and FASTER R-CNN for weapon detection. The input image undergoes a series of processing steps, including passing through a Convolutional Neural Network (CNN) backbone, which is often a pre-trained network like VGG16 in the FASTER R-CNN, which consists of two modules: a RPN (Region Proposal Network) and Fast-RCNN. RPN creates region proposals using the feature maps, these region suggestions are possible object-containing bounding boxes. The RPN works by swiping a small window (usually 3x3) over the feature map, predicting whether an object is present at each position, and then adjusting the bounding box's coordinates accordingly. Anchor boxes, which are pre-defined boxes with varying scales and aspect ratios, are used for this. Based on their objectness scores, a measure of how likely a region proposal will contain an object, the RPN ranks its generation of regional proposals. A predetermined amount of the best-scoring submissions are chosen for additional handling. 

The Fast R-CNN detector processes the chosen proposals, fine-tunes the bounding box coordinates, categorises the content inside each box, and outputs the final object detection results. By using the RPN to propose regions of interest, Faster R-CNN significantly speeds up the object detection process compared to its predecessors like Fast R-CNN, which relied on external methods (e.g., selective search) for generating region proposals. An SSD or Single Shot Detector is designed to efficiently detect objects in a single pass-through, unlike two-stage detectors like Faster R-CNN. A Proposed Architecture to Suspect and Trace Criminal Activity Using Surveillance Cameras. The authors of [2] discuss the steps of processing the information from the CCTV and managing a centralised system for crime management. The research states that each video stream needs to be divided and processed independently. However, the research does not explicitly mention any algorithm that will be used during processing. “Real Time Crime Detection by Captioning Video Surveillance Using Deep Learning” research discusses storing captions of the incident instead of saving the video to save both time and space. The paper suggests using encoder-decoder architecture. An encoder-decoder model is a type of neural network architecture commonly used for sequence-to-sequence tasks, such as machine translation and text summarization. It consists of two main components: an encoder and a decoder. The encoder takes an input sequence and processes it to generate a vector representation of the input. This vector representation captures the meaning and context of the input sequence. The encoder can be implemented using different types of neural networks, such as recurrent neural networks (RNNs) or transformers. The decoder takes the vector representation generated by the encoder and uses it to generate an output sequence. The decoder generates the output sequence one element at a time, using the vector representation and the previously generated elements of the output sequence as input. The decoder is also implemented using different At modern rail stations, ensuring passenger safety and security is paramount. Traditional types of neural networks, such as RNNs or transformers. “Using Machine Learning to Assist Crime Prevention '' The research work aims to predict the pattern and find the hotspots of crime in a city or state. The author employed multiple algorithms, including Random Forest and Naive Bayes, and conducted a comparative analysis of their results. This approach involves applying these algorithms to a dataset or problem and evaluating their performance metrics to determine which algorithm is more effective in achieving the desired outcome. Surveillance systems often face challenges in swiftly identifying potential threats or unusual activities in vast and busy environments. However, integrating machine learning into surveillance cameras revolutionises the monitoring process.

Rail stations can significantly enhance security measures by deploying smart surveillance systems powered by machine learning algorithms. These cameras can autonomously detect suspicious behaviours, such as unattended luggage or individuals loitering in restricted areas. For instance, a machine learning-based camera system can quickly differentiate between regular commuter movement and erratic behaviour, triggering real-time alerts for immediate intervention by security personnel. Moreover, these systems continuously learn and adapt to the station's patterns and dynamics, refining their accuracy in threat detection over time. This bolsters security and optimises operational efficiency by minimising false alarms and focusing human attention where it's most needed.

In essence, the amalgamation of machine learning technologies with surveillance cameras at rail stations marks a substantial leap forward in fortifying security measures while streamlining operations, ultimately ensuring a safer and more efficient travel experience for all commuters.

                                                                                                                       Objective: 
                                                                                                                     --------------
After carefully going through numerous research papers and articles, we got an overview and a good idea about how to approach our problem statement. Weapon detection[1] Can help determine illegal items that may be involved in violence or crime. Using SSD or fast R-CNN [1] is a tradeoff between speed and accuracy which can be further improved by using models like YOLOv3 [5] which we will discuss later. The architecture[2] of a centralised crime management system Can be used for efficient crime management. While the paper[2] outlines the steps of processing CCTV information, a noticeable observation is the lack of explicit mention of the algorithms used. Opens venues for future exploration and discussion of all the algorithm choices in centralised crime management. The shift from storing a video to storing incident captions for real-time crime detection[3] highlights pragmatic approaches to overcoming challenges related to time and space. The use of encoder-decoder Architecture is a noticeable observation, showcasing a thoughtful adaptation of neural network models for processing and summarising the surveillance data. However, it may lack the ability to identify the actions of a human in a crowded environment more accurately which can be further improved by using posture detection techniques. The utilisation of machine learning algorithms for predicting crime patterns and identifying hotspots in a silty or state[4] reflects a proactive approach to crime prevention. The paper's exploration of various algorithms such as random forest and naive bayes introduces a cooperative perspective emphasising the importance of selecting an appropriate model for accurate predictions which can be used with the combination of captioning and capturing the motions of humans, further improving the efficiency of the system. 

                                                                                                                 Detailed Methodology: 
                                                                                                               --------------------------
Our methodology for enhancing surveillance system in railway stations revolves around the integration of advanced machine learning algorithms, particularly focusing on posture tracking for human action detection and activity captioning. The aim is to address existing limitations and improve the precision and efficiency of surveillance systems in identifying potential threats and unusual activities. The overview of our methodology is explained in the flowchart below.

AlphaPose is an advanced deep-learning algorithm used for estimating human poses from images or videos. It accurately identifies key points [9] in the human body and is capable of detecting multiple individuals [12] in a scene simultaneously. AlphaPose operates in real-time, making it suitable for applications like surveillance, action recognition, and sports analytics. Its open-source nature encourages community contributions and customization for specific needs, while its high accuracy and performance make it valuable across various industries.

YOLOv3, short for "You Only Look Once version 3," is a state-of-the-art object detection algorithm. It efficiently identifies objects within images or video frames in real time. YOLOv3 operates by dividing the image into a grid and predicting bounding boxes and class probabilities for each grid cell. Unlike traditional object detection methods[6], YOLOv3 considers the entire image at once, enabling fast and accurate detection of multiple objects in a single pass. This makes it suitable for applications like autonomous driving, surveillance, and image analysis where real-time processing is essential. [5]

The study underscores the paramount importance of leveraging smart surveillance powered by machine learning algorithms to enhance security and operational efficiency across various sectors, particularly in environments like transportation hubs where ensuring safety amidst high traffic volumes is crucial. Implementing machine learning algorithms in smart surveillance systems revolutionises traditional security measures by offering a proactive approach to monitoring and threat detection. These systems analyse visual data captured by surveillance cameras in real-time, enabling the identification of potential threats while optimising resource allocation and operational workflows.

In this study, a comprehensive model employing machine learning algorithms was developed to bolster security measures in the Indian Railways. A subset comprising 30% of images from a diverse range of classes in the surveillance dataset was meticulously selected to evaluate the model's accuracy. The module was trained using the alphapose to detect the movement and actions done by a person. Here is an example of the output of the sample dataset given in the figure and also the process of feature extraction demonstrated in fig. 

As we know [5]YOLOv3 leverages the Convolutional Neural Networks (CNNs) as a fundamental component for feature extraction and object recognition. YOLOv3's object detection capabilities are intricately linked to the integration and optimization of CNNs in its architecture. The sample datasets provided in the input of YOLOv3 are giving the following outputs, given in fig and fig.

In conclusion, the study emphasises the transformative potential of smart surveillance systems powered by machine learning algorithms in fortifying security measures and streamlining operations in transportation hubs and similar high-traffic environments. By providing real-time insights and proactive threat detection capabilities, these systems offer a robust solution to safeguarding public safety and ensuring smooth operational workflows.
          
													  Database:
	                                                                                                -------------
All the detection and identification systems need to use some face dataset for testing the functions. For identity verification and detection systems, large face datasets are gathered, emphasising the importance of extensive training datasets for accurate CNN [1] performance. Well-known datasets such as Object detection models, including YOLOv3 [5], are trained on datasets with annotated images of objects and movement patterns, ensuring diversity in scenarios.

Posture tracking and human action detection, exemplified by AlphaPose, are trained on datasets capturing various human activities in rail stations. Integration involves establishing communication protocols between components, optimising the system for real-time processing, and implementing continuous learning mechanisms.

Testing and evaluation include benchmarking against predefined standards, scenario-based testing for different security threats, and gathering user feedback. Documentation encompasses comprehensive details of the methodology, algorithms used, and integration processes. Reporting includes a detailed summary of results, emphasising improvements in threat detection, reduction in false alarms, and overall system efficiency[15].

In essence, the database strategy ensures that the enhanced surveillance system is well-equipped with diverse datasets, enabling effective training and evaluation of machine learning models, ultimately fostering a safer and more efficient travel experience in rail stations.

                                                                                                       Model Structure:
												    ---------------------
[3] This model structure is used for ConvLSTM.The ConvLSTM model structure integrates convolutional and LSTM layers to process sequential data with spatial and temporal dependencies.[3] It combines convolutional operations with LSTM units, enabling the model to capture both spatial and temporal patterns simultaneously. Input data undergoes feature extraction through convolutional layers, while LSTM cells handle memory and state management to capture long-term dependencies.[3] The model is trained using gradient-based optimization algorithms and finds applications in video analysis, weather forecasting, and medical imaging. Once trained, it can be deployed for tasks like video prediction and anomaly detection. Here is the flowchart of input and output and the modules used in the feature extraction.
We can determine that the local CCTV surveillance system is set up using a local system like a pc or a laptop. Then the footage from the CCTV system is uploaded to the allocated private server. The uploaded data or footage of the CCTV system is stored in the DSU (Datacenter Storage Unit), which can be accessed later for the detection of crowds or the prevention of crime using the Real Time Video Processing module that was created by our team utilising machine learning. If too many people are detected , an alert for crowd detection, and if any physical violence is detected it sends an alert for crime prevention both of which are then sent to the officials. The alerts that are sent; on the detection of any anomaly to the local device of the security personnel which can be accessed by them using the designated app on the local device. The location of the anomaly is sent to the mobile phone of the security official on duty, connected to the WIFI of the railway station allowed only to the security officials..


                                                                                                        Results:
												     --------------
This study gives an appraisal of recent object detection and anomalous movement detection methodologies, development of smart surveillance of CCTV in crowded areas like railway stations and the challenges faced during the creation of the project. A comparative analysis [8] is provided to both obtainable databases and connected benchmarks. We have highlighted the shortcomings of the older projects, and evaluated a way to deal with the limitations.


                                                                                              Performance of approaches used:
											   ------------------------------------
A Total loss vs Total validation loss graph is generated by our model using the testing dataset, 
convLSTm
LRCM approach
 
                                                                                                     Observation :
												  -------------------
Solution for improving the system:
Our ongoing research on posture tracking for human action detection and activity captioning introduces a novel dimension to security applications by addressing the limitations in existing research, the project aims to enhance the precision and efficiency of the surveillance systems. Notably, the survey identifies the need to overcome specific challenges in previous works. The litany Of existing methodologies and applications discussed in the literature survey offers a valuable backdrop for identifying gaps and challenges. The absence of explicit algorithms in detail in certain studies and the evolving need for more precise human action detection underscore areas for improvement and further investigations.

                                                                                                    Conclusion:
												  ---------------

The overarching objective of this project is to design, implement, and deploy an Artificial   Intelligence (AI) and Machine Learning (ML) based smart surveillance system with a focus on enhancing crowd management, security measures, and resource allocation. The specific objectives are outlined as follows: 

Real-Time Crowd Management: Develop and implement an ML model capable of real-time crowd analysis. The model will approximately count the number of people in public spaces and trigger notifications to authorities when predefined thresholds are surpassed. The aim is to facilitate timely responses for effective crowd management, particularly in crowded areas such as railway stations. 

Enhanced Security Measures: Leverage AI to identify potentially violent human actions, detect suspicious activities, and monitor sudden movements. The objective is to enhance security through real-time alerts and insights, enabling security personnel to proactively address security threats, prevent incidents, and maintain a secure environment.

Integration with Existing Infrastructure: Ensure seamless integration with current CCTV systems in railway stations and other relevant locations. The project aims to overcome compatibility challenges, allowing the smart surveillance system to complement and enhance existing infrastructure without disruptions. 

Cloud-Based Scalability and Adaptability: Implement the smart surveillance system using cloud computing for optimal scalability and adaptability. The objective is to enable the system to efficiently process data without additional hardware installations, making it easily scalable for deployment in various settings beyond railway stations, such as airports, government buildings, and public gatherings. 

Seamless Implementation and Adoption: Ensure a seamless implementation process, considering factors such as stability, reliability, and ease of integration. The objective is to deliver a solution that can be adopted smoothly by authorities, minimising disruptions to existing operations. By achieving these objectives, the project aims to significantly contribute to the improvement of security and operational efficiency in public and private sector domains, providing a robust and adaptable smart surveillance system. 

                                                                                                       Reference:
												     ---------------
1. Jain, H., Vikram, A., Mohana, Kashyap, A., Jain, A.: "Weapon Detection using Artificial intelligence and deep learning for security applications." Telecommunication Engineering, RV College of Engineering, Bengaluru, Karnataka, India (2020).
2. Naurin, S. T., Saha, A., Akter, K., Ahmed, S.: "A Proposed Architecture to Suspect and Trace Criminal Activity Using Surveillance Cameras." In: Editor, F., Editor, S. (eds.) CONFERENCE 2020, LNCS, vol. 9999, pp. 1–13. American International University, Dhaka, 
   Bangladesh. Date: 5 June 2020. Springer, Heidelberg (2020).
3. Nayak, N., Odhekar, S., Patwa, S., Roychowdhury, S.: "Real Time Crime Detection by Captioning Video Surveillance Using Deep Learning." Information Technology, VESIT, Mumbai, India. Date: 7 July 2022.
4. Lin, Y.-L., Chen, T.-Y., Yu, L.-C.: "Using Machine Learning to Assist Crime Prevention." In: 9th International Proceedings on Proceedings, pp. 1–2. Department of Information Management, Yuan Ze University, Taoyuan City, Taiwan (2017).
5. Redmon, J., Farhadi, A.: "YOLOv3: An Incremental Improvement.
6. Arun Hampapur, Lisa Brown, Jonathan Connell, Sharat Pankanti, Andrew Senior and   YingliTian. Smart Surveillance:- Applications, technologies and implications.    Researchgate.January  2004. 
7. Dayana R, Suganyam M, Balaji P, Mohammad Thahir A, Arunkumar P. Smart surveillance     system using Deep Learning. International Journal of Recent Technology and Engineering. May2020 .
8. Icshan taufic, Maya Mushthopa, Aldy Riadly, Muhamad Ali Ramahani, Yana Aditia Gerhana, Narang Jsmail. Comparison of Principal component Analysis algorithm and local binary pattern for feature extraction on face recognition system. MATEC Web of conferences. January 
   2018 
9. Ivan Ozhiganov. Convolution neural network vs cascade classifiers for object detection. DZone. May 2017.@
10. Kelvin salton do prado. Face Recognition on Understanding LBPH Algorithms. Towards Data Science. Nov 2017. 
11. Mrinal Tyagi. HOG (Histogram of oriented gradients): An overview. Towards Data Science. July 4 2021.
12. Paul Viola, Michael Jones. Rapid Object Detection Boosted a cascade of simple features. Researchgate. May 2004.
13. Wang D, Tang J, Zhu W, Li H, Xin J, He D. Dairy goat detection based on Faster R-CNN from surveillance video. Comput Electron Agric. 2018;154:443–9 (ISSN 0168-1699).
14. T. Sultana and K. A. Wahid, "IoT-Guard: Event-Driven Fog-Based Video Surveillance System for Real-Time Security Management", IEEE Access, vol. 7, pp. 134881-134894, 2019.
15. Kardas K, Cicekli NK. SVAS: surveillance video analysis system. Expert Syst Appl. 2017;89:343–61.
