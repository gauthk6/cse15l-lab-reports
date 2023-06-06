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
