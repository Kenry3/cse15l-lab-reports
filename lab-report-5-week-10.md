# Week 10 Lab Report #

![](bsr.png)
*By using bash for loop and <span style="background-color:cyan">`>`</span> command, I save the output of running each file by provided MarkdownParse and my own MarkdownParse into <span style="background-color:cyan">`results.txt`</span> and <span style="background-color:cyan">`results2.txt`</span>, then I use <span style="background-color:cyan">`diff`</span> to compare the outputs, and here is the display on the terminal:*

![](diff2.png)

*The test file that causes two different output:*

![](li.png)

*According to the preview, <span style="background-color:cyan">`link`</span> is regarded as a link with <span style="background-color:cyan">`\(foo\)`</span> as its URL.*

*Therefore, the implementation from provided MarkdownParse seems to be correct since it correctly prints out <span style="background-color:cyan">`\(foo\)`</span>*

*The problem with my code is that it just simply checks location of first <span style="background-color:cyan">`)`</span> and includes the content within <span style="background-color:cyan">`()`</span>*

![](mycode.png)