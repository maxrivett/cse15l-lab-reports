# Lab Report 4, Week 8

*In this lab, I will be remotely testing my markdown-parse and the markdown-parse that I reviewd in lab on Wednesday (the CSE 15L version). I will be writing three tests for each, testing three snippets that were given to me as part of this report, and then analyzing how the programs did.*

I started by **cloning my and the course staff's versions of markdown-parse** into my ieng6 remote server.
![cloning](/images/labreport4/pic1.png)
<br><br>

I then added the three snippets provided as markdown files in my markdown-parse
![add snippets to mine](/images/labreport4/pic2.png)
and in the other markdown-parse
![add snippets to other](/images/labreport4/pic3.png)
<br><br>

Then, I tested the three snippets on the (CommonMark Demo Site)[https://spec.commonmark.org/dingus/] to see which of the code in the snippets should appear as links. 
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
and the course staff's version failed on two of the three
![testing](/images/labreport4/pic9.png)
<br><br>