# **Week 3 Lab report**

## *Part 1*
### *Add*
![Add](/week3-screenshots/cse15l-week3-step2.png)
```
if (url.getPath().contains("/add")) {
    String[] parameters = url.getQuery().split("=");
    if (parameters[0].equals("s")) {
        added.add(parameters[1]);
        return parameters[1] + " has been added!";
    }
}
``` 

The program tries to read the path in the url and if its add, it performs the add function. It reads the query and splits it up at the equals sign. So you'll have an string array called parameters where at index 0 you'll have "s" and index 1 as the string you want to add to a string arraylist called added. Then program stores the string into added and prints out a statement saying that the string inputted has been added.


<br />

### *Search*
![404 Error](/week3-screenshots/cse15l-week3-step3.png)
```
else if (url.getPath().contains("/search")) {
    String[] parameters = url.getQuery().split("=");
    if (parameters[0].equals("s")) {
        String result = "";
        String search = parameters[1];
        for(int i = 0; i < added.size(); i++){
            if(added.get(i).indexOf(search) != -1){
                result = result + added.get(i) + " ";
            }
        }
        return result;
    }
}
```
Search does the same as add where it looks for the /search path and splits the queury into two parts at the equals. However, for the search function, the second part of parameters is the string you are searching for. The for loop loops through the arraylist added, where you stored all of your added values, and adds each element that contains the searched string to a string called result. The if statement is what filters the added list and only adds values that contain the searched string. Result is then printed and it contains all of the elements that have the searched string. 

<br />

### *404 Error*
![404 Error](/week3-screenshots/cse15l-week3-step1.png)
```
 return "404 Not Found!";
```
If the path is neither /add or /search, the program returns a 404 error message.

<br />

## *Part 2*
### *ArrayExample: reversed( )*
Failure-inducing test:
<br />

![Failure-inducing test](/week3-screenshots/cse15l-week3-step4.png)
<br />


Symptoms:
<br />

![Symptoms](/week3-screenshots/cse15l-week3-step5.png)
<br />

Bug:
<br />

![Bug](/week3-screenshots/cse15l-week3-step6.png)
<br />

The problem in the code is that it is storing the elements in the newArray into arr. It should be the other way around as by doing it this way you are taking the null elements from the new empty array, reversing them, and putting them into the original array. Thats why the symptoms show that although we expect 3, it returns 0. What you should do is taking the elements from the old array, reversing them, and storing them in the newArray. Finally the returned array should be the new one as it is the ones that has stored the correctly reversed values.

<br />

### *LinkedArrayExample: length( )*
Failure-inducing test:
<br />
![Failure-inducing test](/week3-screenshots/cse15l-week3-step7.png)
<br />

Symptoms:
<br />
![Symptoms](/week3-screenshots/cse15l-week3-step8.png)
<br />

Bug:

![Bug](/week3-screenshots/cse15l-week3-step9.png) (NOT AVAILABLE)

I wasn't really able to find any bugs specifically with the LinkedListExample methods. However my issue was that whenever I would try to add in anything more than two nodes to my linkedlist, such as in the screenshot shown, the test would take like 3 minutes to run and spit out a OutOfMemoryError. I genuinely don't know why this is considering it is only 3 nodes and also it makes it basically impossible for me to test anything.