# Abandoned_object_detection
The objective of the project is to identify abandoned objects that are left by unknown person in high traffic areas.

I came up with implementing an "Abandoned Object detection" by reading a [Research paper](https://www.researchgate.net/publication/343422224_Abandoned_Object_Detection_using_Frame_Differencing_and_Background_Subtraction?_tp=eyJjb250ZXh0Ijp7InBhZ2UiOiJwdWJsaWNhdGlvbiIsInByZXZpb3VzUGFnZSI6bnVsbH19) . So, the idea is to detect abandoned objects that are left by some strangers and alert security people that there is an object left at the particular place. This will be really helpful to identify if there are any suspicious activities or threats around Railway Station, Malls, etc .,

The implementation is purely based on OpenCV (no pre-trained models are used) and no pre-trained Deep Learning models are used.

## Library used: OpenCV, numpy
## Tested on Data: Aboda dataset and PETS 2006 data

The key steps to detect Abandoned objects are as follows:
## 1. Background learning model:
The background model is learned from the initial frames of the video
## 2. Detecting New objects:
Once the Background is learned, objects that appear in the frames are detected and the objects can be anything such as a person, a bag, etc., This is done using Frame Differencing Technique.
## 3. Object Classification:
All the objects, either it is moving or static object is detected. Now, we will have to classify that if the object is abandoned or not. The position history of objects are stored and if the object remains static for some time duration, it is declared as Abandoned object by the algorithm. In my case, it was a bag which is correctly identified as an Abandoned object when it is left by a stranger.

However, the project currently works on static cameras only. I will take this as an improvement to make the project to work on Moving cameras as well. 
