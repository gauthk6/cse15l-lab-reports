# Lab Report 5:

## 1. Student Question
Hi! I am currently on a MacOS system running Visual Studio Code from my local computer. Specifically, I am trying to run the grade.sh script from a modified version of the 
CSE 15L Skill Demonstration 2 code. However, when I run the grade.sh script on the github repository that contains my code with the following command: ```bash grade.sh https://github.com/gauthk6/list-examples-duplicates.git```, I unfortunately get the following error message which is contained in the screenshot below:

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/c471d286-3bea-4117-84d2-b30c21104cbf)

Based on what I understand, it seems that I am dealing with an ArrayOutOfBounds error, which means that I might be trying to access an index that isn't contained within the input ArrayLists that are fed to both the failing tests. However, I just can't figure out how to fix this!

## 2. Orginal TA Response
Greetings! Usually, when an ArrayOutOfBounds error occurs, there is some sort of issue with the logic you wrote to iterate through the ArrayLists. As such, can you please go through that logic one more time, and see if there is any scenarios where your code tries to access an index that is greater than the length of the ArrayList minus one? Remember, ArrayLists are zero-indexed, meaning that the first index is 0! As such, the problem might be that your are trying to access an element at the index corresponding to the length of the ArrayList, which is greater than the length of the ArrayList minus one! As such, that might be the root cause of your ArrayOutOfBounds error.

## 3. Student Response
Wow, I didn't know that! It turns out, you were right! I was looping through my input list and checking every index, including list.size()! As such, that was causing the ArrayOutOfBounds error. Now that I have changed that error, and rerun the grading script, I pass all the tests! Thanks for the help! Attached is a screenshot of the intended behavior.
![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/1cee16c3-b0f4-46f2-bd74-a56082b6a102)

## 4. Overview
The file and directory structure needed was acquired by cloning the following git repository by using the following command: ``` git clone https://github.com/ucsd-cse15l-s23/grader-skill-demo2``` and this give us the following directory structure:

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/20d484cf-a275-4e32-b2b0-a98cb6e46d98)

After that, in order to run the grading script, I used the following command: ```bash grade.sh https://github.com/gauthk6/list-examples-duplicates.git```. The bug in the submission program was on line 13 in the screenshot below, where the termination condition was: ```i <= list.size()``` which caused the ArrayOutOfBounds error.

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/07064f9b-9536-4cd3-90c3-3cd799161b06)

The series of commands that I ran to demonstrate the bug were:
```git clone https://github.com/ucsd-cse15l-s23/grader-skill-demo2```
```bash grade.sh https://github.com/gauthk6/list-examples-duplicates.git```

and the above screenshot from the "student" demonstrated that behavior. Moving on, we fixed the issue by simply deleting the equals sign on line 13, making the termination condition: ```i < list.size()``` as it should be. Running the bash script again on this updated submission, we get the response that all tests passed as seen above.




