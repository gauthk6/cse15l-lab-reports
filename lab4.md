# Lab Report 4

## Step 4: Log into ieng6
For this step, I entered the following command in the terminal: ```ssh cs15lsp23ge@ieng6.ucsd.edu``` and got the following output:

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/562336ef-8768-4caa-80e2-04bbff87e974)

In order to do this, I kept hitting ```<up>``` and ```<down>``` keys until I got to the previous instance of running the above command.


## Step 5: Clone your fork of the repository from your Github account
For this step, I entered the following command in the terminal: ```git clone git@github.com:gkishore6/lab7.git``` and got the following output:

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/cc6b6ee7-7ae5-4564-bce0-5081b8a0df9f)

For this step, I simply went to my fork of the repository on GitHub, and copied the ssh link, and then ran the above command in the terminal.

## Step 6: Run the tests, demonstrating that they fail
For this step, I entered the following command in the terminal: ```bash test.sh``` and got the following output:

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/a4282b1f-97f6-4d46-bd45-2b3b90008584)

For this step, it was yet another simple one, as I just needed to run the given script, so I ran the above command in the terminal without needing to navigate through much else.

## Step 7: Edit the code file to fix the failing test

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/5f0603d7-9fff-44be-9743-ea652b14c571)

For this step, I edited the code file to fix the failing test. In order to do so, I first openeed the file in vim, using the ``` vim ListExamples.java``` command. Once vim was open, in order to make the neccesary changes I hit the following series of commands: ```<43> <j> <e> <r> <2> <:wq>```. These commands did the following, ```43``` is the line number, ```j``` goes to the next line, ```e``` is the next command, ```r``` replaces a character of text, ```2``` is the character that I want to add in the place of 1 (as in index2 v.s index1) , and ```:wq``` is the last command that exits vim.


## Step 8: Run the tests again
For this step, I entered the following command in the terminal: ```bash test.sh``` yet again and got the following output:

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/9b908f46-5335-4ccd-be03-f032d449a4bd)

For this step, I kept hitting the ```<up>``` key until I got to the previous instance of running the above command. As we can see, all of the tests pass now!

## Step 9: Commit and push the resulting change to your Github account

![Image](https://github.com/gauthk6/cse15l-lab-reports/assets/58676663/c04142d6-08ec-4379-ad25-cd6758c23ca2)

