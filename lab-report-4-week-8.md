# Week 8 Lab Report #

>Click the [link](https://github.com/Kenry3/markdown-parse) to my markdown-parse repository

>Click the [link](https://github.com/clingunis/markdown-parse) to reviewed markdown-parse repository

## Snippet 1 ##

**the preview of Snippet 1**
![](/image/s1.png)

*So the expected output of our markdownParse program should be <span style="background-color:cyan">``[`google.com, google.com, ucsd.edu]`` </span>. So I create a test:*
![](/image/t1.png)

*And the terminal displays*

**My code**
![](/image/p2.png)

*Reviewed code*
![](/image/p5.png)

*The test failed for both programs since our code didn't check for backticks. Thus, the list includes element that's not supposed to be there*
![](/image/tf1.png)

**The possible code change:**
1. create variables <span style="background-color:cyan">`bS`</span> and <span style="background-color:cyan">`bE`</span> representing the start of backticks and the end of backticks
2. add <span style="background-color:cyan">`if`</span> statement to check if the index of <span style="background-color:cyan">`bS`</span> is smaller than the index of <span style="background-color:cyan">`nextOpenBracket`</span>
3. if it is smaller and the index of <span style="background-color:cyan">`bE != -1`</span>, then search the <span style="background-color:cyan">`nextOpenBracket`</span> after the index of <span style="background-color:cyan">`bE`</span>

## Snippet 2 ##

**the preview of Snippet 1**
![](/image/s1.png)

*So the expected output of our markdownParse program should be <span style="background-color:cyan">`[a.com, a.com(()), example.com]` </span>. So I create a test:*
![](/image/t2.png)

*And the terminal displays*

**My code**
![](/image/p3.png)

**Reviewed code**
![](/image/p4.png)

*The test failed for reviewed programs since their code just simply check if the link is in the format <span style="background-color:cyan">`[]()` </span>*
![](/image/tf2.png)

**The possible code change:**

1. find the closest <span style="background-color:cyan">`nextOpenBracket`</span> to the <span style="background-color:cyan">`nextCloseBracket`</span>
2. check if it is locating after <span style="background-color:cyan">`\`</span>

## Snippet 3 ##

**the preview of Snippet 1**
![](/image/s3.png)

*So the expected output of our markdownParse program should be <span style="background-color:cyan">`[https://ucsd-cse15l-w22.github.io/]` </span>. So I create a test:*
![](/image/p1.png)

*The test failed for both programs since our code didn't take the empty new line and link starts with <span style="background-color:cyan">`http or https` </span> into consideration
![](/image/tf33.png)
**The possible code change:**

1. if there are empty new line, use <span style="background-color:cyan">`continue` </span> and set current index to the start index of non empty new line

2. Before adding links to list, use method <span style="background-color:cyan">`trim()` </span> on element

3. check if string starts with <span style="background-color:cyan">`http or https` </span>

