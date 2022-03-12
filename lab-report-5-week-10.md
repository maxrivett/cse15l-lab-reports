# Lab Report 5, Week 10

*In this lab report, I will be choosing 2 of the 652 commonmark-spec tests where my group's implementation of markdown-parse had a different result than the implementation provided. Then I'll compare them and see which implementation handled the test better and why.*
<br><br>
**Tests I Chose:**
<br>
I chose to analyze tests number 142 and 143 (corresponding to `142.md` and `143.md`).
<br><br>
**How I Found Them:**
<br>
I found them by comparing the results of running the script file on my `markdown-parse` and the course staff's `markdown-parse`. I used `time bash script.sh`:![time bash](images/labreport5/pic1.png)
<br>
Then I put it in a text file `results.txt` by using output redirection: ![output redirect](images/labreport5/pic2.png)
<br> ![output redirect2](images/labreport5/pic3.png)<br>
Then I used the `diff` command to see how the results differed: ![diff](images/labreport5/pic4.png)<br>
As you can see, the 98th line and the 100th line yielded different results, so I investigated...<br>
![investigation](images/labreport5/pic5.png)<br>
I found that line 98 corresponded with test file `142.md` and 100 with `143.md`
<br><br>
**How They're Different:**
<br>
As you can see above, my implementation says that the is a link "x" in both of the files, whereas the course staff's implementation does not show a link.
<br>
Here is the code for the two files:
![file1](images/labreport5/pic6.png)
![file2](images/labreport5/pic7.png)
<br>
I found this by accessing the files through vim.
![vim](images/labreport5/pic8.png)

<br><br>
**Which Implementation (if either) is Correct?**
<br>
For Test 142:
Looking at the code, the **course staff's implementation is definitely correct**. There is no link in this file, and yet my implementation shows there being one.

<br>
For Test 143:
Looking at the code, the **course staff's implementation is definitely correct**. There is no link in this file, and yet my implementation shows there being one.
<br><br>
Here is my code: 
![my code](images/labreport5/pic9.png)
<br>
I think the problem is that my implementation does not check if there are square brackets before the parentheses, which allows something like this to happen. I think that would be a relatively quick fix, involving adding a check that there is an open and closed square bracket before the parentheses.
<br><br>
*Thanks for reading and have a nice spring break!*