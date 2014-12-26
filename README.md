BackgroundTask
==============

This Android library introduce some reactivity to working with threads. 
Idea is close to «RxJava», but rx library was so «heavy» for me, so I needed to find something more simplier. 

### Main idea
Standard Android tools help you to do some simple works in background, but it becomes much more complicated when you have to
handle big amounts of data, when you want to show progress of handling and especially when there is high probability of
exceptions to be thrown.

I found these problems makes my life not so colorful as I want:
* need to recreate AsyncTask for every execution
* difficult access to UI elements
* painful handling of exceptions
* and as result, AsyncTask not guarantee you that your task will be done

And there is idea of the library:
* you have some «source objects», in example, image urls
* you want to get some «result objects» from sources — Bitmap objects from urls
* then you create SourceHandler<String, Bitmap> object, that can make image from url
* you create ResultHandler object, where you can do anything with obtained image and UI-thread
* you create ErrorHandler, where you can handle your exceptions and errors
* after this you create «BackgroundTask» with Source, Result and Error handlers



### Features
Library is small but gives you some cool features:
* Handling 
