# FingerDetector

This program is created to detect and count the number of upright fingers. It consists of two stages:-

a)Palm detection

In this stage the palm is detected using Google's mediapipe. It uses machine learning to track the movements of your palm using 21 reference points. It is made with the help of mediapipe(https://google.github.io/mediapipe/solutions/hands) a library built by google.

Download mediapipe with the following command- 

```
pip install mediapipe
```

The palm is tracked using 21 reference points. These reference points are predefined. The reference points are as follows-

![image](https://user-images.githubusercontent.com/47482433/121740885-5bd25a80-cb1b-11eb-8501-9270fb396746.png)

b)Finger detection

We will use the coordinates of the reference points of the plam to determine whihc finger is upright and which is not. This will be achieved by taking the distances between the hand landmarks on each finger.

Example output:-

All fingers-

<img width="479" alt="allFingers" src="https://user-images.githubusercontent.com/47482433/127780268-2b757b0c-3fa4-4fd6-9af0-fcea1e4226c0.png">

Thumb, index finger and pinky-

<img width="479" alt="threeFingers" src="https://user-images.githubusercontent.com/47482433/127780276-cfb887a1-d072-4afc-b511-6ec2acc5e737.png">

After executing the program a camera window will open up, you will be able to see your palm being tracked in this camera window. The top right corner will show you the number of upright fingers and the names of the upright fingers.

Libraries used-> opencv(cv2), mediapipe, math.

