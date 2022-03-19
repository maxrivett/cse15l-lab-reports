# Lab Report 4, Week 8

*In this lab, I will be remotely testing my markdown-parse and the markdown-parse that I reviewed in lab on Wednesday (another group's markdown-parse). I will be writing three tests for each, testing three snippets that were given to me as part of this report, and then analyzing how the programs did.*

I started by **cloning my and another group's versions of markdown-parse** into my ieng6 remote server.
<br>
Links to each:<br>
[My markdown-parse](https://github.com/maxrivett/markdown-parse)<br>
[Other groups's markdown-parse](https://github.com/yi113/markdown-parse.git)
<br>
![cloning](/images/labreport4/pic14.png)
![cloning](/images/labreport4/pic10.png)
<br><br>

I then added the three snippets provided as markdown files in my markdown-parse
![add snippets to mine](/images/labreport4/pic2.png)
and in the other markdown-parse
![add snippets to other](/images/labreport4/pic13.png)
<br><br>

Then, I tested the three snippets on the [CommonMark Demo Site](https://spec.commonmark.org/dingus/) to see which of the code in the snippets should appear as links. 
<br>
**Snippet 1** (Note that `cod[e` and `code]` are both hyperlinked, it just may not appear so from the screen capture.)
![snippet testing](/images/labreport4/pic4.png)
<br>
**Snippet 2**
![snippet testing](/images/labreport4/pic5.png)
<br>
**Snippet 3**
![snippet testing](/images/labreport4/pic6.png)
<br><br>

Once I knew which segments of code to expect as links, I added three new tests to each of the markdown-parse versions with these links being expected in the test. 
![testing](/images/labreport4/pic7.png)
<br><br>

My markdown-parse version ended up failing on all three tests
![testing](/images/labreport4/pic8.png)
and the other group's version failed on two of the three
![testing](/images/labreport4/pic9.png)
<br><br>

**Now, to answer some questions that were posed to me as part of the lab report:**

1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.
<br>
My Response: *Yes, I think there is. My program failed because it did not recognize that the backtick inside the square brackets was closing an earlier backtick which should have created a small code block. A way to fix this could be to have a boolean flag that sets to true whenever a backtick code block is opened, then back to false when it is closed. This way, you can see if the link has part of it that is meant to be a code block.*
<br><br>
2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.
<br>
My Response: *Yes, there must be a relatively quick fix because the other group's program handled this snippet well. I think a way to go about this could be to check if there is another closed parenthesis directly after the one we are examining and going to use as the closing parenthesis, and if so, keeping going and use that one. This would solve the problem, as my code failed this snippet because it marked the link as a.com(( when it should have been a.com(()).*
<br><br>
3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
<br>
My Response: *Yes, I think there is a small fix that could be made. I think the fix would be to check for an empty line within the brackets, and if there is one, automatically disqualify it from being considered a link.*
<br><br>

*Thank you for reading!*