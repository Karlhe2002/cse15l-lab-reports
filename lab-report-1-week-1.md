# Lab-report week 1

## Installing VScode (Part 3)
![VScode homepage](https://user-images.githubusercontent.com/106074396/193361724-6da9cebe-d6c8-4b3d-b132-8fcdf9b502ae.png)
I think for this step most of the people have already done before this class. If you haven't done yet, go to the webpage [Installing VScode](https://code.visualstudio.com/). Follow the instructions and do it.

## Remotely Connecting (Part 4)
![Remoteconnect](https://user-images.githubusercontent.com/106074396/193363469-50374e0c-5479-4c1c-9dc6-b3cdd9dad085.png)
For this step, you need to open a new termianl in your VScode. Then, using the command "ssh" and your account to login the remote computer. For me, it is "ssh cs15lfa22nc@ieng6.ucsd.edu". After login, you will see the page shown above. 

Compared to the other group numbers' screenshots, we all have the same table-"Cluster Status", with the same Hostname, but different Time, #User, Load, and Averages value. Since people have different computers and differnt operation system. It is reasonable that is different.

## Trying Some Commands(Part 5)
![Remote commands try](https://user-images.githubusercontent.com/106074396/193365395-8ab6152e-320f-4c54-a437-2513b7f18e8a.png)
The picture shown above is some of the commands I tried in the remote computer, such as "cd", "cp","ls" and so on.

![Commands try 1](https://user-images.githubusercontent.com/106074396/193365958-e55795fa-28fc-4419-a47e-cefa35efff60.png)
Then, I logged out. Try some of the commands on my own computer. Since my opertion system is windows, so I found that the command "ls" and "dir" give the same result to me.

![Commands try 2](https://user-images.githubusercontent.com/106074396/193366231-2dee182e-6481-4719-a941-b57cd528e64e.png)
Also, I tried to use the comman "pwd" and "cat". However, because it cannot print the picture successfully, it doesn't run. I use the "cd" change directory successfully to the different files.

## Moving Files with scp(Part 6)
![WhereAmI 1](https://user-images.githubusercontent.com/106074396/193369547-f1c8ac60-af60-4e71-8c5d-e8d6b33023c0.png)
For this part, you need to first creat a java file in your computer named WhereAmI. We have learned that from CSE11 classes. Then, you are able to use the VScode terminal to compile the file, and run the file, like the screenshot I shown above. The command to compile java file is "javac <'file'>". The command to run the file is "java" with file name.  

![WhereAmI Remote](https://user-images.githubusercontent.com/106074396/193370184-9cbae008-fae8-4c02-ace1-4e558431e438.png)
Then, after you creating this file successfully on your computer. You are asked to send your code to the remote computer. However, the first thing you need to make sure is where you save your file on your computer. You need to change the directory to the file, which have "WhereAmI". For me, it is on the Desktop. After that, using the scp command to copies files from your computer to the remote. "scp <'file1'> <'file2'><'username'>@<'servername'>:<'path'>" This is the command for that. Then, you can compile and run it in the remote computer.

The difference is that we use different operating systems. It shows us the different properties of the different computers. When I use it as a client, it shows the remote computer’s property-"Linux". On my laptop, it shows mine. I think “getProperty” is a built-in method in Java, just like System.out.println(). It shows us the properties of the different objects. 

## Setting an SSH Key
![key](https://user-images.githubusercontent.com/106074396/193377117-29126afa-b9e1-4fc3-86a6-57392b4551e1.png)
![Window step](https://user-images.githubusercontent.com/106074396/193383793-ad3322fe-5ab3-4f70-b8f3-2b129a6b8006.png)
![image](https://user-images.githubusercontent.com/106074396/193384156-1052f6a2-00a6-4801-b3c2-b28b3df9dbfd.png)
I follow all the step in this section, but I failed to add-ssh for the windows operation system.
I tried both the Windows step and the normal step on website.
For the windows step on that website method, it said that permission was denied. 
For the normal step you teach, it said no such file and directory.
I hope later I get a chance to get my keys step done.

## Optimizing Remote Running
![kuai](https://user-images.githubusercontent.com/106074396/193384500-c8a834ab-d60b-46a5-baa7-c30a767f0220.png)
This is the first method to make you write less code. You can write a command in quotes at the end of the command. Like I did, “ls” at the end of ssh command. It really get faster.

![image](https://user-images.githubusercontent.com/106074396/193384520-610088ba-112c-4af7-bddd-afc89c6c65f9.png)
This is the second method to make you faster. You can use semicolons to run multiple commands on the same line. My keystroke really decrease a lot.