# Lab-report week 5
## Find
## -empty
-empty: means find the empty file in this directory

1. Check the empty files in this directory. For now, there is only one file named "./find-result.txt"
![image](https://user-images.githubusercontent.com/106074396/198898854-30881e84-fd42-4357-aa3a-a595c6ab5539.png)

2. Now, I use the mkdir to create a empty file, named "23473820.txt" so that now there are two empty files find in this directory.
![image](https://user-images.githubusercontent.com/106074396/198905801-cf182778-ede5-4966-a97e-0ca9506e3ee5.png)

3. Here, I use mkdir and vim make an empty and a not empty file. Then, I use the -empty to search the whole file, to check if the empty file increases only once. 
![image](https://user-images.githubusercontent.com/106074396/198906764-f459299e-976a-441c-b0d5-cac4d1896466.png)

This method is really useful because sometimes 

## -type

1. . -type f: for this command, find only print the files in this directory. It can let us know how many files in this directory.
![image](https://user-images.githubusercontent.com/106074396/198906397-72b1a22e-9bcf-49d6-8fb2-09126240c3ad.png)
![image](https://user-images.githubusercontent.com/106074396/198906451-f71b4158-92ef-4ec2-b1e0-e81686996404.png)

2. . -type d: for this command, find only print all the directories in the technical/ directory. It is useful since we don't need to use "dir" all the times, instead we can directly get a file path.
![image](https://user-images.githubusercontent.com/106074396/198907403-a767bb79-e176-475b-b9c6-eae26e4b6ff2.png)

3. . -type p: for this command, find only print all the pipe in this directory. So, p refers to the pipe here. It is useful since we can know how many pipes in this files. For here, there are no pipes.
![image](https://user-images.githubusercontent.com/106074396/198907732-7810324f-f265-4ffc-a43a-16dfc67019e1.png)

## -size 
1. . -size -3k
This means we check the file that smaller than 3k.
![image](https://user-images.githubusercontent.com/106074396/198908444-f68b9b72-e553-44eb-bab2-242c39a5c87b.png)

2. . -size -429k
This means we check the file that smaller than 429k.
![image](https://user-images.githubusercontent.com/106074396/198908491-f45b1446-40bd-4d4e-a5c0-9d8b83801276.png)
![image](https://user-images.githubusercontent.com/106074396/198908554-1cbde596-0bf0-43d1-b2cb-6949e6a61e94.png)

3. . -size +3k
This means we check the file that larger than 3k.
![image](https://user-images.githubusercontent.com/106074396/198908912-ce295272-8c1c-40dc-8d28-1eeed2f9ef83.png)
![image](https://user-images.githubusercontent.com/106074396/198908959-1de510cb-1a6f-4bba-9b3c-f702843d0dd9.png)

It is useful since when we need to find some files with the given range. Then, we can use this command to find all the conincident files. 
