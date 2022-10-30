# **Week 5 Lab report**

## *`grep` command line options*
### *`grep -l`*
![-l ex1](/week5-screenshots/cse15l-week5-step1.png)
<br />

So what -l does is that it only returns the files that match with the searched for input. This is useful as you won't have the duplicate output of lines that contain the keyword in the same file. In this case you search for the phrase "base pair" in any `.txt` file in `technical/plos/` and it returns 2 files. Without the `-l` there would be 3 lines of outpus as "base pair" exists in two different lines in one of the files.

<br />

![-l ex2](/week5-screenshots/cse15l-week5-step2.png)
<br />

In this example, we still search for "base pair" but through all the `.txt` files in `technical/biomed/` instead. Another difference with using `-l` is that since your searching for files, you save output as it doesn't print out the specific lines in these files that have the keyword. This command shown prints out a long list of files that contain "base pair".

<br />

![-l ex3](/week5-screenshots/cse15l-week5-step3.png)
<br />

In this screenshot, its the same as the last two. I use `-l` for the keyphrase "100% of" for all the .txt files in `technical/biomed/`.

<br />

### *`grep -i`*
![-i ex1](/week5-screenshots/cse15l-week5-step4.png)

<br />

So what `-i` does is that it ignores upper and lower case for the input and returns both upper and lower case results. This is useful if you want to check for both upper and lower case keywords in one go. In this case you search for the phrase "inos" in all the `.txt` files in `technical/biomed/`. Without the `-i` there would only be the lines containing all lowered cased "inos", but as shown in the output, it returned lines that included "iNOS" as it ignores cases.

<br />

![-i ex2](/week5-screenshots/cse15l-week5-step5.png)

<br />

In this case, I search for "inos" on the files in `technical/plos/`. The interesting thing for this example is that it doesn't differ from not using `-i` as there are no appearances of variations of different capitalizations of "inos" in this path.

<br />

![-i ex3](/week5-screenshots/cse15l-week5-step6.png)

<br />

In this case, I search for "1005" on the `.txt` files in `technical/plos/`. For this example it shows that capitalizations don't work for numbers. So I expected it to print out lines that included "100%" as shift + 5 would be % but I found out `-i` doesn't work this way. The command returned nothing as there are no `.txt` files in this path that contain "1005".

<br />]

### *`grep -n`*

![-n ex1](/week5-screenshots/cse15l-week5-step7.png)

<br />

What `-n` does is that it shows you the line number for the matching lines. This is useful as it helps you find the exact line in a file that matches your keyword. In this case you search for the phrase "inos" in any `.txt` file in `technical/plos/`. Without the `-n` it would be the same just without showing the line numbers behind where it shows which file it is.

<br />

![-n ex2](/week5-screenshots/cse15l-week5-step8.png)

<br />

Similarly to above, I searched for "iNOS" in any `.txt` in `technical/biomed/`. The returned is the same as without a command line option, just with the line number shown.

<br />

![-n ex3](/week5-screenshots/cse15l-week5-step9.png)

<br />

I searched for the first line of a specific file in `technical/biomed/` and it showed that the line number was 6, as all the `technical/biomed/` files start at line 6.

<br />