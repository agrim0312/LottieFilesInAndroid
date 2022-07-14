# LottieFilesInAndroid
This is a step by step guide on how to insert lottie animations into your android project 

This is assumed that you had created a project and using Android Studio as your default IDE

STEP-1
From your project structure panel, select your projects build.gradle file and add the following lines inside your dependencies block
```
def lottieVersion = "3.4.0" 
implementation "com.airbnb.android:lottie:$lottieVersion"
```
>Update lottieVersion to the latest one

STEP-2

> If you want your lottie to be load via internet 

Add LottieAnimationView to your activity_main.xml file inside the layout where you want to place it 
```
<com.airbnb.lottie.LottieAnimationView
     android:id="@+id/animationView"
     android:layout_width="match_parent"
     android:layout_height="wrap_content"
     app:lottie_url="REPLACE_JSON_URL"
     app:lottie_autoPlay="true"
     app:lottie_loop="true"/>
```

STEP-3
> If you need your animations to work offline, you can bundle your animations with your application by including them in your projects resources directory .

download the animation in json or in zip format 
```
<com.airbnb.lottie.LottieAnimationView
    android:id="@+id/animationView"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    app:lottie_rawRes="@raw/animation"
    app:lottie_autoPlay="true"
    app:lottie_loop="true"/>
```
replace *@raw/animation* with *@res/your-amination-file-name* 

**Your first Android project with Lottie animations is ready to go!**

source code-https://lottiefiles.com/blog/working-with-lottie/getting-started-with-lottie-animations-in-android-app
