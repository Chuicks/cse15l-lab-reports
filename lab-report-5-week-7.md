# **Week 7 Lab report**
## Part 1
### *Changing the name of the start parameter and its uses to base*

<br />

`cd week6-skill-demo1<enter>vim TestDocSearch.java<enter>/0<enter>xi391<escape>:wp`

<br />

### `cd week6-skill-demo1 <enter>`
![cd](/week7-screenshots/cse15l-week7-step1.png)

<br />

You use `cd` to go to the directory week6-skill-demo1.

<br />

### `vim TestDocSearch.java <enter>`
![vim](/week7-screenshots/cse15l-week7-step2.png)

<br />
This command opens the file TestDocSearch.java with vim mode, which allows you to edit it directly from the terminal. Vim mode is shown in the bottom half of the screenshot.

<br />

### `/0 <enter>`
![search](/week7-screenshots/cse15l-week7-step3.png)

<br />

`/0` searches for the first occurance of 0 in the file that you have opened up in vim. As shown in the screenshot, the first appearance is now higlighted, the "0" of "10 total files to search".

<br />


### `xi391 <escape>`
![edit](/week7-screenshots/cse15l-week7-step4.png)

<br />

Here `x` deletes the higlighted element so "10 total" turns to "1 total" then `i` sets vim to insert mode befor the cursor. Then typing 391 inserts it to where the cursor is so "1 total" becomes "1391 total". After that the ` <escape> ` exits vim mode and you get what the screenshot shows.

<br />


### `:wq`

![:wq](/week7-screenshots/cse15l-week7-step5.png)

<br />

`:wq` saves and exits vim and kicks you back out to the terminal.

<br />

## Part 2
### Timings
already logged into a ssh session: 

scp local file:

### Questions
*Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?*
<br />

I would prefer to edit locally first and then scp it over. Although it does take longer to do, I just much more prefer editing with the vscode. 

---

*What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)*