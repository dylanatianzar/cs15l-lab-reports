# Lab 5 Report Dylan Atianzar A17609722
## Turning Lab 4 into a Bash Script
For this task, I revisited my Lab 4 Report. By looking through each command, I turned the commands from Lab 4 into a bash script.
First, I created a local .sh file titled **"LabFourInBash.sh"**. Then, I put the commands into the bash script and tested it locally. This had worked
locally, but Lab 4 is about connecting to the ieng6 server and performing the commands. 

Initially, I had just put the  `ssh login` command at the beginning;
however, that wasn't working because it wouldn't perform the commands automatically. I ended up looking up and finding that in order to process the
commands automatically after login, I had to add them on the same line as the ssh login. This meant my final bash script looked like this:

`ssh cs15lwi23arg@ieng6.ucsd.edu 'rm -rf Lab5Report; mkdir Lab5Report; git clone git@github.com:dylanatianzar/lab7.git Lab5Report; cd Lab5Report; javac -cp  .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests; sed -i '43s/index1/index2/' ListExamples.java; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java; java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests; git add --all; git commit -m "Fixed error using bash"; git push origin main; exit;` 
all in one line.

Because I had set up all my ssh keys from that lab, I was able to directly log into the ieng6 server from the command and use the ssh version of git clone instead
of the https link. Through the ssh version, I was able to push and commit the changes that I had made to ListExamples.java .

The output of running the script ended up looking like this:
![Image](https://user-images.githubusercontent.com/69043855/224892313-e6d74f16-3cb4-441b-beef-8c47c8547a00.png)

Another of the main issues I had to was finding how to fix the bug in the code without editing it myself, but I eventually found
the  `sed` command would help when using the bash script. This class has helped me in the ability to turn a process into just a simple script that I 
am able to run. 
