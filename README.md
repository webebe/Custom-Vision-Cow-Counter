# Custom-Vision-Cow-Counter
Using Python with OpenCV and a trained model in Azure Custom Vision to detect cows in a moving drone video. The project is based on the Counting Cars project from IBM available here https://github.com/IBM/powerai-counting-cars. Instead of using the stand alone PowerAI Software, I trained a object detection model in the Azure Custom Vision environment. Cows are detected using the provided API calls to my model. The code splits the input video into single frames and labels them accordingly. Detected objects are tracked from frame to frame in order to avoid counting them multiple times. Detected cows are increment the "Cows-in-sight" counter, when a cow is lost the counter decrements.
Detection of Cows is quite challenging for the Azur detection algorithm because of cow overlays in the video.

The detection model was trained with 25 manually labeled images from the video, but from a section not used to test the model. The detection algorithm therefor has never seen the frames from the video before.

Check out the result:
![Alt Text](https://github.com/webebe/Custom-Vision-Cow-Counter/blob/main/cows1.gif)
