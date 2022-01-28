# Lab Report 2, Week 4

*In this lab report I will be showcasing three code changes I made to fix bugs in the initial code we were given.*
<br><br>
For each code change, I will...
<br>
* Show a screenshot of the code change diff from Github (a page like this)
* Link to the test file for a failure-inducing input that prompted you to make that change
* Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)
* Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.
<br>
-------------------------------
<br><br>
1.**BUG 1**
<br>Here is a screenshot of the code change diff from Github:
![Test 1 Commit](images/labreport2/test1commit.png)
<br>[Test File for Break 1](lab-report-2-files/test-break-1.md)
<br>
Here is an example of the output before I fixed the bug:
![Test 1 Fail](images/labreport2/test1fail.png)
And after I fixed the bug:
![Test 1 Pass](images/labreport2/test1pass.png)
<br>
In this case, the bug is that the program is producing an infinite loop. The symptom is that we are not checking to see if there is another open bracket in the code. This produces an infinite loop due to the failure-inducing input that is referencing test-break-1.md.
<br><br>
2. **BUG 2**
<br>Here is a screenshot of the code change diff from Github:
![Test 2 Commit](images/labreport2/test2commit.png)
<br>[Test File for Break 2](lab-report-2-files/test-break-2.md)
<br>
Here is an example of the output before I fixed the bug:
![Test 2 Fail](images/labreport2/test2fail.png)
And after I fixed the bug:
![Test 2 Pass](images/labreport2/test2pass.png)
<br>
In this case, the bug is that the program is producing an infinite loop. The symptom is that we do not have a boolean flag that can be called on when certain processes occur which would result in a bug if not for the flag. This produces an infinite loop due to the failure-inducing input that is referencing test-break-2.md.
<br><br>
3. **BUG 3**
<br>Here is a screenshot of the code change diff from Github:
![Test 3 Commit](images/labreport2/test3commit.png)
<br>[Test File for Break 3](lab-report-2-files/test-break-3.md)
<br>
Here is an example of the output before I fixed the bug:
![Test 3 Fail](images/labreport2/test3fail.png)
And after I fixed the bug:
![Test 3 Pass](images/labreport2/test3pass.png)
<br>
In this case, the bug is that the program is producing an infinite loop. The symptom is that we are not checking to see if there is an exclamation point before the first open bracket, which would make it an image file rather than a link. This produces an infinite loop due to the failure-inducing input that is referencing test-break-3.md.
<br><br>