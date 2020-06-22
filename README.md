# PushNotificationAndroid
Sending push notification to Android devices using python server 

Notification can be sent to any Android or iOS device using Firebase and pyfcm. 

You need to create an account on firebase console, enable GCM and get the server key for authentication on python server. On Android or iOS device get the token(Unique identification key for that perticular device). Send that key to server side in background for initiating push notification to the device from python backend. 

In the dependencies part of the build.gradel file add 

 classpath 'com.google.gms:google-services:4.3.3'

Make sure google() is added under repositories in allprojects part of the build.gradel file.



Now you make changes in build.gradel(:app). Add following plugin below apply plugin: 'com.android.application'.

apply plugin: 'com.google.gms.google-services' 

Now under dependencies add 
 implementation 'com.google.firebase:firebase-messaging:17.3.4'
 
 
You need to add google-services.json file generated from firebase console while creating app on firebase in app folder. 


