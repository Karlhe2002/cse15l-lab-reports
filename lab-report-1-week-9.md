# Lab-report week 8

## Code
```
# Create your grading script here
rm -rf student-submission
git clone $1 student-submission

cp TestListExamples.java student-submission

cd student-submission

if [[ -f ListExamples.java ]]
then
    echo "All files are found!"
else
    echo "Files was not found!" 
    exit 0
fi

javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java 


if [[ !$? -eq @ ]]
then
    echo "Compile Error!"
    exit 1
else
    echo "Compile successfully!" 
fi

java -cp .:../lib/hamcrest-core-1.3.jar:../lib/Junit-4.13.2.jarorg.junit.runner.JUnitCore TestListExamples > TestResults.txt

echo "Tests ran!"
cat TestResults.txt
erromessage=$(grep -i "Tests run:" TestResults.txt)

if [[ $erromessage == "" ]]
then
    echo "Good Job! TEST PASSED!"
else
    echo "Failed!"
    echo $failure
fi
```

## Screenshots of the server run
![d14f1dd8b91f915636ca675fc7cbd2d](https://user-images.githubusercontent.com/106074396/204064063-bcc6b277-92b9-4570-a76a-18eb1286d0e5.jpg)
![5072b6762edc1dfe32597c46a8b5c13](https://user-images.githubusercontent.com/106074396/204064070-0bfc6de2-aa03-42cc-b5c2-6260d88fd2a8.jpg)
![38df6ce074b6d9d289d956b840327ac](https://user-images.githubusercontent.com/106074396/204064072-abc5b19f-6761-4859-9f42-6fb234601378.jpg)

## Trace my code

For here, I take https://github.com/ucsd-cse15l-f22/list-methods-filename student submission as an example.

1. This line refers to clear the student submission first. It let us to grade on the new students submission, instead of the old one.
The stdout and the stderr are both nothing. The return code are supposed to be 0.
```
rm -rf student-submission
```

2. This line refers to git clone the students submission to the students-submission, the place we can run it. $1 is the parameter refers to the link when we bash it.
The Stdout is nothing. The stderr should be Cloning into 'student-submission'... The return code is also 0.
```
git clone $1 student-submission
```

3. These lines refer to copy and change the directory where we need to work. Both of them the stdout and stderr are nothing. Also, the return code are supposed to be 0.
```
cp TestListExamples.java student-submission
cd student-submission
```

4. This is the if statement line to check if the right file contained. For here, since we don't have the right file here. The if statement doesn't meet. So, we go to the else statement. 
```
if [[ -f ListExamples.java ]]
```

5. The else statement will first echo the "Files was not found!" like the results I shown above. Also, it will exit. So, it will not run the following code anymore. Here, the stdout is "Files was not found!". The stderr is nothing. The return code is 0.
```
else
    echo "Files was not found!" 
    exit 0
```