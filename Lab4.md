# Lab 4 Report Dylan Atianzar A17609722
## Task Competition Reproduction
## Step 4: Log into ieng6
Keys pressed: `<up><enter>`
The `ssh` command used to log into the ieng6 machine was 1 up in the search history, so I used the up arrow to access it. 

![Image](https://user-images.githubusercontent.com/69043855/221689755-a77cb52d-18ca-4d1f-8a2d-fc0c63fa0c23.png)

## Step 5: Clone Lab 7 Repository Fork
First, I typed out `git clone ` in my terminal. Then, I clicked my browser, clicked the green `<> Code` button in the fork and copied the ssh clone using `ctrl-c`.
Then, I went back to the terminal and pressed `<right-click-on-mouse>` to paste it into the terminal with my previous `git clone` command and `<enter>`.
![Image](https://user-images.githubusercontent.com/69043855/221690439-15efdeb4-ee16-47c0-92e7-fb34be40346c.png)

## Step 6: Run the tests, demonstrating that they fail
First, I typed `ls` to make sure the fork was cloned. Then, I used `cd` to access the folder and used `ls` again to see the file names and on the lib folder
to see the .jar file names. Then, I typed the command `javac -cp .:./lib/hamcrest-core-1.3.jar:./lib/junit-4.13.2.jar *.java` to compile all the files.
Then, I typed the command `java -cp .:./lib/hamcrest-core-1.3.jar:./lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` to run the
tester file.
![Image](https://user-images.githubusercontent.com/69043855/221693276-c9981b1b-1504-4409-beba-2cf8b40974e1.png)

## Step 7: Edit the code file to fix the failing test
First, I typed `cat ListExamples.java` to see the code of the java file to spot the error. Then, I spotted the error in the last while loop, so I used the
`nano ListExamples.java` command to edit the file. I pressed `<down>` until I got to that line and `<right>` until I got to the word index1. 
I pressed: `<backspace> 2` to replace the "1" with a 2 and `<ctrl-o><enter><ctrl-x>` to save the changes and exit the nano command. 

![Image](https://user-images.githubusercontent.com/69043855/221698898-d1c2348d-bd81-4753-8119-fcbc9f4da69e.png)
![Image](https://user-images.githubusercontent.com/69043855/221699197-279f7783-2461-4f0f-84e6-e0f53f33479f.png)
## Step 8: Run the tests, demonstrating that they now succeed
Keys pressed: `<up><up><up><up><enter>`, `<up><up><up><up><enter>`
The `javac -cp .:./lib/hamcrest-core-1.3.jar:./lib/junit-4.13.2.jar *.java` was 4 up in the history, and so I used the up arrow to access it. After
running that command, I did the same thing for the `java -cp .:./lib/hamcrest-core-1.3.jar:./lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
command because it was 4 up in the history.

![Image](https://user-images.githubusercontent.com/69043855/221696019-ed1263e2-8fd5-494d-8b2e-a659e39a64e8.png)
## Step 9: Commit and push the resulting change to your Github account
Commands typed: `git add --all`, `git commit -m "Fixed error"`, `git push origin main`
The **first** command is used to put all the modified files into the git history. The **second** command is used to make a local version of the repository
with those files and a message to describe what I changed with those files. The **third** command is used to replace the files on the Github repo with the
new version of the files I just committed.

![Image](https://user-images.githubusercontent.com/69043855/221697365-cd530384-38d6-4dde-951c-e3e525b58f42.png)
