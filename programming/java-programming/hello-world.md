# Hello World

In this lesson, we will go over how to set up VSCode and use it to write and execute Java programs.

#### Why use VSCode?

Visual Studio Code is a Java IDE, or integrated development environment (it works with other programming languages too, but we're just using it for Java). In other words, it's software that includes many software development tools that makes programming far more convenient. VSCode in particular has several advantages. It is both free and highly customizable, and also offers built-in support for robot programming tools. The above benefits make VSCode our preferred option when writing robot code.

**Installing VSCode and Getting Started**

If you read What is Java? (which you should have), then you know that to write and run Java code, you need a JDK installed. Thus, our installation process takes 3 steps: 1) Installing VSCode 2) Installing a JDK 3) Configuring VSCode to use the JDK.

To complete step 1, Visual Studio Code can be installed at [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download).

To complete step 2, a JDK can be installed at [https://adoptium.net/](https://adoptium.net/).

Step 3 is a bit more complicated. Firstly, open VSCode. You should see a screen like this:

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Go to the left taskbar and click on the Extensions icon (last one).&#x20;

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

You can install an extension by clicking the Install button on the bottom right of each extension. For our lessons, two extensions are necessary: The "Java" extension and the "Extension Pack for Java" extension.&#x20;

After installing the Java extension, a tab called "JDK Downloader" may open. This tab is what lets VSCode run the JDK you've installed on your machine. Click "Select installed JDK from my system" and navigate to the folder where your JDK was installed.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

If this tab does not appear automatically, press Control + Shift + P  and type "Download, Install, and Use JDK".&#x20;

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Finally, to make a project, you can navigate to the Extension icon (first one) and click the Create Java Project button. For the project name, pick whatever makes sense to you. It is important to give your projects meaningful names to keep your code organized in case you need to look back at it. I suggest you name this project "HelloWorld".

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Congrats! You have made your first project in VSCode.

#### A Tour of VSCode

Projects in VSCode are stored in folders that contain many subfolders and Java files. For right now, the only folder that should concern you is the src folder, where you'll store all the Java files you code. For right now, it should only contain either the `Main.java` or `App.java` file, which should look something like the above.

There are a few important parts of the VSCode interface that you should know about.

The left side of the screen has a thin, vertical strip that contains a couple of icons. The topmost icon is Explorer, which is responsible for showing/hiding the files in your project. The second icon is Search, which allows you to find specific lines of code throughout your project (compared to Control + F, which only finds lines in a single file). The third icon is Source Control, which we elaborate more on [here](https://docs.iowacityrobotics.org/programming/version-control). The fourth icon is Run and Debug, which as the name suggests, runs and debugs your project. For the rest of the lessons, the other icons should be unnecessary.

The bottom of the screen should be taken up by the Terminal (which should automatically open when you run your project). Here, you can see the results of running your project.

One last thing of note to learn are commands. You can navigate to the File tab on the top and click Open Folder to open pre-existing projects, or simply type Control + K and Control + O in succession. You can navigate to the search bar on the top to open files in your project, or simply type Control + P. Finally, you can also use Control + Shift + P  to run additional commands, such as compiling your project.&#x20;

When you are ready, you can run the program by going to the Run and Debug icon. After a few seconds, you should see the text `Hello, World!` appear in the terminal (note that there might be a few lines of gibberish before it). Congratulations on running your first bit of Java code! At this point, you can confirm VSCode is working properly.

Take a few minutes to explore the VSCode interface. Make sure you're comfortable with creating projects, locating existing projects, and running your code. Once you feel ready, you can move on to the next lesson. There, you'll start learning to actually write code!
