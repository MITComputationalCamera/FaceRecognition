FaceRecognition (HW4)
===============
You should now be set up to run OpenCV on Android. Remember to install OpenCV Manager on your device (Google Play Store) or emulator (Google this, you can use "adb install")

Your task is to modify the Android+OpenCV code hosted on Github to implement an app to distinctly recognize your specific face as compared to other faces. That is, instead of simply recognizing a face, the app will idenitfy your face and draw a red rectangle around it instead of a green rectangle.

1. Take an image of your face and crop it to be similar to "myface.jpg" as shown in `res/drawable/myface.jpg`

2. Import the project above into Eclipse (if you are on Mac, you will have delete the ".cmd" again to get it to build correctly [Right Click Project>Properties> C/C++ Build> Build Command])

3. Change the path of the file Android.mk inside the jni folder to match the location of your OpenCV path
	ex: it will be ( ../../sdk/native/jni/OpenCV.mk ), change it to the folder path in your computer that contains the file OpenCV.mk 
				or
		you can copy the project at the same locations of the openCV samples. 

4. Verify that the OpenCV reference is correct 
	- Right click the project-> proprieties -> Android -> Library 
	- If this is wrong, remove the reference and add the right library (your library)
		
5. Add your code in between the comments (HomeWorkChanges) inside the `onCameraFrame` function in the `FdActivity` class.
	- try to use the functions in OpenCV. Almost all steps can be executed using OpenCV functionality.
	
>IMPORTANT: This app will ONLY work when you hold the phone in landscape mode. This is because of how it is trying to recognize face in an absolute manner.
>Specifically, if you hold the phone in portrait mode, it sees :) instead of '__' and thus does not recognize a face.

>NOTE: This app does very very basic face recognition and will not always work accurately. However, you will notice dramatic improvements if you stay in a similar 
>environment to your myface.jpg picture and tweak the threshold coefficient. 
 
TIPS
====

- Use the image that you took of your face to debug. Show the image you created (myface.jpg) on your computer monitor and try to detect the face from within your app 
  - We're doing this because of the nature of this solution to face recognition. Here, the results can vary according your facial expression, lighting conditions etc. Thus, testing it on this image should eliminate those factors.
		
- If you already have the face-detection sample of OpenCV installed and the launch on the device is not succeeding because of conflicts, try deleting the sample face-recognition app from your phone.  	
		

Extra Credit (+10pts)
====================
- search/propose and create a method to get a more general face recognition algorithm to recognize your face in different conditions.  

Submission
==========
MIT/Skoltech Students: Please upload your .apk file and your myface.jpg file to the Stellar site. I will try the app out on your myface.jpg file against other sample face images I also have (displaying on a computer monitor).

Online Students: Upload your .apk to the Google Play Store and show off what you've built with some screenshots on the Facebook page!