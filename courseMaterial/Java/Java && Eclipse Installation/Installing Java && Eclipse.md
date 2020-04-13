# Installing Java && Eclipse 

### Video Guide: 

These video guides are slightly dated with the specific version, but so long as you download the latest`java JDK` you can follow the rest of the video and be completely fine for the java installation. In the  video tutorials for installing eclipse, you're better off downloading the installer and following its prompts.  

* **Windows: **Here is a [link](https://www.youtube.com/watch?v=5UHV0mrhTjM) to a video that is a great tutorial on how to install java, OR if you'd like, please follow the steps below: 
* **Mac:** Setting up java on a mac is a bit more straightforward, but [here](https://www.youtube.com/watch?edufilter=NULL&v=fAE-dnVUTs0)'s a video nonetheless. 

Note: it is possible to have eclipse run both c++ and java. I will note, that it does take some fiddling with the program to get it to easily run both. I will gladly help if you would like to try to have a single program run both, but it is also significantly easier to just download a "java" eclipse (instructions below).  





## Java Development Kit

It's likely that you already have the java run time installed on your system (you need it to run and use eclipse for c++). In order to use Java for development, however, we'll need the java JDK (java development kit). 

### Download and Installation

To get the JDK, either [click here](https://www.oracle.com/technetwork/java/javase/downloads/jdk12-downloads-5295953.html) for java 12, or go to google and search java jdk. That will take you to a list of sites. Feel free to download whichever version you'd like greater than 8. The most recent version at the time of writing this is Java 12 (Note: if you wish to use a version of java older than the current, you will have to register with oracle). 

You can download either a zip file containing all of the binaries of Java, or an installer. Downloading the installer is recommended. Make sure to choose the right operating system as well. Once finished downloading, run the installer. 

### Path Variables

In order to get java to run once you've installed it, we need to add it to our path variables: 

- **Windows**
  - Open your file explorer and navigate to your `C:\Program Files`. In your program files, you should find a directory called `java`. In your `java` directory, you should see a file called `jdk.SOMEVERSIONNUMBERS` where `SOMEVERSIONNUMBERS` is the version of java you downloaded. Copy the path to that directory. 
  - Navigate to your System Properties. Click on the advanced properties link/tab/button (depending on which windows OS you're running), and click on `Environment Variables`. Once there:
    - Add a variable `JAVA_HOME` with the value you copied from your  `C:\Program Files\Java\jdk.WhateverVersionYouDownloaded `
    - Open your Path variable, and add to the end of it: `;%JAVA_HOME%`
  - Once finished. Open a command prompt (click the windows home button, search for `cmd` ). After opened, type `java -version`. You should see your newly installed java's version get printed out. 
- **Mac**
  - You shouldn't have to add any specific variables, however, to make sure that your java is properly running, open your terminal (cmd + space then type terminal). Once your terminal is opened, type `java -version` and `javac -version`. Both should respond with the versions of your newly installed java. 



## Eclipse

To download eclipse, we need to first go to Eclipse's [homepage](https://www.eclipse.org/).  On their homepage, click the download button to get the downloads page :

![Screen Shot 2019-08-22 at 7.07.36 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.07.36 PM.png)

Navigate again to the eclipse application's download page and click the download button: ![Screen Shot 2019-08-22 at 7.10.36 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.10.36 PM.png)



Once you've downloaded the eclipse installer, open it. You should see: 

![Screen Shot 2019-08-22 at 7.16.18 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.16.18 PM.png)Once run, the installer will prompt you on what you'd like to install. Choose the Eclipse IDE for java developers: 

![Screen Shot 2019-08-22 at 7.16.37 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.16.37 PM.png)

Once clicked (this is the portion that may cause the most headaches), you ought to see two fields that are already prepopulated: `Java1.8+ VM` and `Installation Folder`. If the fields are not prepopulated, it is likely the case that your path variables are not properly working. If you're unable to get your installer to recognize your recently downloaded JDK, please contact me as quickly as possible.  ![Screen Shot 2019-08-22 at 7.17.12 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.17.12 PM.png)

Click install, and agree to the terms and conditions. 





Once installation is finished, you may wish to move your eclipse application around. 

### Windows: 

If you're on a windows machine, you'll find that eclipse had been downloaded as a whole directory. Navigate into the `Installation Folder` directory, and you should see an `eclipse.exe` file. That is the executable which runs eclipse. Create a shortcut if you like, or just navigate to that directory whenever you wish to open eclipse. 

### Mac: 

 If you're on a mac, navigate to the directory where you installed the `Installation Folder`. You should see a directory called `eclipse`:  ![Screen Shot 2019-08-22 at 7.22.33 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.22.33 PM.png)Click into the eclipse folder, and you should see a versioned folder in your directory. Navigate into that folder: ![Screen Shot 2019-08-22 at 7.22.45 PM](/Users/mjlane/Desktop/Screen Shot 2019-08-22 at 7.22.45 PM.png)This is where the eclipse application lives. You can access it from here, OR you can drag and drop it into the applications folder (recommended for application searching via the spotlight search). 

With that, your eclipse should be up and running!  