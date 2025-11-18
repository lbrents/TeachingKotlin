# Creating A New Project

### Android Studio

As you might have guessed, Android Studio is the application we will be using to create and edit our programs. Don't worry about the finer details quite yet. Just know that it is very nice to use.

### Ok Actually Creating A Project Now

If you don't have it open already, open up Android Studio. Hopefully only one of two things can happen. Ideally, you will be greeted by the following image. If not, then ask for help or something idk.

![Something](../Images/AS_01.png)

From here, follow these steps.

1. Click on "New Project"
2. Select "No Activity"
3. Click "Next"
4. In the name section, type in something you will remember
5. Click "Finish"

Once that is done being created (it takes a while), you will enter the editor where all the magic happens with a clean project.

### Our Entry Point

Before we actually start learning how to code, we need to create a file to serve as the starting point for our program.

To the left of the editor, there should be a file explorer window with two folders. One should be "app" and the other "Gradle Scripts". We don't care about the second one.

Expand the folders the same way as shown in the following picture and the locate the empty "com.example.[whatever name you made]" folder. Make sure it is the folder with no parenthesis after it.

![Something](../Images/AS_02.png)

Once you find that folder, right click it and select New > Kotlin Class/File and then a little window should pop up. For the name, type in `Main.kt` and make note of the capitalization here. And lastly, select "File" and then press enter.

Your new file is made, but there is unfortunately still one last step before you get to move on. This next skill is probably the most important for **every single programmer** out there. Copy and paste the following code into the `Main.kt` file.

``` kotlin
fun main() {
    println("Hello, world!")
}
```

(The joke was copying and pasting because we do that a lot, very funny)

The following image should be what your final result looks like!

![Something](../Images/AS_03.png)

To test if everything is working as it should be, please click the green button to the left of the code you pasted and select "Run". If everything went well, then a window should open up at the bottom of the screen with the text "Hello, world!". From now on, you can also click the green run button at the top right corner of the editor as well to run your program.

... And finally, we shall learn how to print.

<p align="right">
    <a href='Printing.md'>Printing</a>
</p>

___

<p align="center">
    <a href='../README.md'>Table Of Contents</a>
</p>