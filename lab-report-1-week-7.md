# Lab-report week 7

## Part1

Task: Changing the name of the start parameter and its uses to base

- git clone our whole package into the remote computer.
- cd to the File DocSearchServer.java
- /start<Enter>   

We first serach where "start" is. Then, press <Enter> moving our cursor to the fisrt time of the place where "start" appears. 
![image](https://user-images.githubusercontent.com/106074396/201453270-33e69dce-049a-4268-be2a-cc2180951fc1.png)
- ce

The command c means we change the word we chose.
The command e means we choose to the end of the word that the cursor choose.
They also leads us to the INSERT mode of vim.
![image](https://user-images.githubusercontent.com/106074396/201453561-5f20bbc5-a935-44af-b609-5e3dab92215c.png)

- "base"

Type "base" 
![image](https://user-images.githubusercontent.com/106074396/201453742-aa10bfa8-ae9e-4250-9365-2e39ef8362df.png)


- <Esc>
Quit the INSERT mode, back to the noraml mode.

- n.n.n.

The command n means moves the cursor to the next search.
The command . means repeat what we have done for the last editing.
When we have repeat these two commands for couple times, we will see "E486: Pattern not found: start", by complementing the command n. For here, we successfully change all the "start" into "base".

![image](https://user-images.githubusercontent.com/106074396/201453976-0812cc95-a340-4b9b-a998-ee7b426aacce.png)

- <Shift+;> which is ":"
- wq <Enter>

The command ":wq" means we first save and then quit the vim, which makes us to save our changes of this file.
![image](https://user-images.githubusercontent.com/106074396/201454146-a58d34ef-d622-46ad-a688-75071a2c8804.png)

This is the whole step of the completing this task.

/start<Enter>ce"base"<Esc><Shift;>wq<Enter>

## Part2

For me, the task is here is shown above, changing the all "start" into "base".

- Method 1:
Edit in VS code, by using <ctrl F> and change it. Then, scp the whole file. Log in and bash the test.sh.
The whole process takes nearly 2 minutes for me to complete the changing.

- Method 2:
Use the vim. Run the command above.  
/start<Enter>ce"base"<Esc><Shift;>wq<Enter>
It only takes me 28 seconds to complete.

For me, I prefered to use the second VIM methods to change it for the future edit. For now, I cannot use the vim very professionally, but it has been faster than change it in local computer. It is much faster than I thought. Also, sometimes remote computer has the different operation system with our own computers. In this week lab, I met a problem of that. Sometimes, when we scp Windows files to the reomote computer, it cannot run it successfully. So, I highly recommanded to use the VIM to edit the file in remote computer.

If the task is a very large task or debugging the program, I might choose to run it in local computer, because we are more familiar with that and also the VS code has the package to help us find the bug very quickly. If it is some small changes or editing, I will definitely choose the VIM mode to edit. It is much faster than change it in local and scp it.