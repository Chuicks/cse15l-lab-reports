# **Week 7 Lab report**
## Part 1
### *Changing the name of the start parameter and its uses to base*

<br />

```
cd week6-skill-demo1<enter>
vim DocSearchServer.java<enter>
/start<enter>
dwibase<escape>
ndwibase<escape>
ndwibase<escape>
ndwibase<escape>
:wq<enter>
```
<br />

### `cd week6-skill-demo1 <enter>`
![cd](/week7-screenshots/cse15l-week7-step1.png)

<br />

You use `cd` to go to the directory week6-skill-demo1.

<br />

### `vim TestDocSearch.java <enter>`
![vim](/week7-screenshots/cse15l-week7-step2.png)

<br />
This command opens the file DocSearchServer.java with vim mode, which allows you to edit it directly from the terminal. Vim mode is shown in the bottom half of the screenshot.

<br />

### `/start <enter>`
![search](/week7-screenshots/cse15l-week7-step3.png)

<br />

`/start` searches for the first occurance of start in the file that you have opened up in vim. As shown in the screenshot, the first appearance is now higlighted, the "start" of "getFiles(Path start)".

<br />


### `dwibase <escape>`
![edit](/week7-screenshots/cse15l-week7-step4.png)

<br />

Here `dw` cuts from the highlighted posistion to the end of the word so "(Path start)" turns to "(Path )" then `i` sets vim to insert mode befor the cursor. Then typing base inserts it to where the cursor is so "(Path )" becomes "(Path base)". After that the `<escape>` exits vim mode and you get what the screenshot shows. Now the first occurance of start is changed to base.

<br />

### *3x* `ndwibase<escape>`  
![edit](/week7-screenshots/cse15l-week7-step6.png)

<br />

Here `n` searches for the next occurance of start. Then `dwibase` does the same as earlier and replaces start with base. This is done 3 times to replace all occurances of start in the file with base.

<br />

### `:wq`

![:wq](/week7-screenshots/cse15l-week7-step5.png)

<br />

`:wq` saves and exits vim and kicks you back out to the terminal.

<br />

## Part 2
### Timings:
already logged into a ssh session: 1:30

scp local file: 1:45

### Questions:
*Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?*
<br />

I would prefer to edit locally first and then scp it over. Although it does take longer to do, I just much more prefer editing with vscode than vim. 

<br />

---

<br />

*What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)*
<br />

If it is just editing one file, they have similar speeds. Though if it is for a large directory, its easier to just use vim directly as scp does only one file at a time which is way slower. Also I am worse at using vim than a normal text editor so naturally I would prefer using the one im more comfortable with.
