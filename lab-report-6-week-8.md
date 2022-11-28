# **Week 8 Lab report**
## grade.sh code block

<br />


```
rm -rf student-submission
git clone $1 student-submission
cp TestListExamples.java student-submission/
cd student-submission

if [[ -e ListExamples.java ]]
then
javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java
java -cp .:../lib/junit-4.13.2.jar:../lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore TestListExamples
else
        echo 'ListExamples.java not found'
        exit 1
fi
```

<br />

## Student submission screenshots
### Missing semicolon
![semicolon](/week8-screenshots/cse15l-week8-step1.png)

<br />

Here the student submission doesn't compile as there is a semicolon missing.

<br />

### All Correct
![correct](/week8-screenshots/cse15l-week8-step2.png)

<br />
Here the student submission is run through all the tests and all three tests pass as shown.

<br />

### Not Found
![missing](/week8-screenshots/cse15l-week8-step3.png)

<br />
Here the file ListExamples.java is not found directly in student-submissions.

<br />

## Trace for Not Found
<br />

```
rm -rf student-submission`

git clone $1 student-submission`
```

Standard output: Cloning into 'student-submission'...

Standard error: repository 'https://github.com/ucsd-cse15l-f22/list-methods-nested' not found

Return Code: 0 

```
cp TestListExamples.java student-submission/
cd student-submission
```
Return Code: 0 


```
if [[ -e ListExamples.java ]]
```

Condition is false as ListExamples.java could not be found as it was in a nested directory

```
then
javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java
java -cp .:../lib/junit-4.13.2.jar:../lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore TestListExamples
```
Then doesn't run as if statement evaluates to false.

```
else
        echo 'ListExamples.java not found'
        exit 1
fi
```
Else runs as if statement evaluates to false.

Standard output: (Whatever is printed out from the tests running)

Standard error: ListExamples.java not found

Return Code: 1 

So when the `git clone` command happens, it outputs Cloning into 'student-submission'... ,  then as the if statement evaluates to false as it couldn't find ListExamples.java, it outputs ListExamples.java not found.