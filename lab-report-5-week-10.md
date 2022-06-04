# Lab Report 5

## How I found the tests
<br />

I found the tests that created different outputs for the given MarkdownParser and our MarkdownParse using vimdiff on the results.txt files that I created for the given MarkdownParser and for our group MarkdownParser. 
<br />
<br />


## Links to test files with different results 
<br />

Test 41
<br/>
[markdown file](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/41.md)
<br/>
[html.test](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/41.html.test)
<br/>
<br/>

Test 481
<br/>
[markdown file](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/481.md)
<br/>
[html.test](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/481.html.test)
<br/>
<br/>
<br/>

## Actual outputs vs Expected
<br/>
<br/>

The given MarkdownParser was correct for test 41 because it returned "[]" with the given file but it was incorrect for test 481 because it returned "[]" for the given file when it should have returned "[/uri]".

Our group MarkdownParser was incorrect for test 41 because it returned "[[url &quot;tit&quot;]]" when it should have returned "[]" and it was incorrect for test 481 because it returned "[/uri "title"]" when it should have returned "[/uri]".

(given MarkdownParser on the left, our group MarkdownParser on the right)
![pic](vimdiff.PNG)

<br/>

The expected output based on CommonMark was "[]" for test 41 and "[/uri]" for test 481
<br/>
### Test 41
![pic](commonMark41.PNG)
### Test 481 
![pic](commonMark481.PNG)
<br/>
<br/>

### Given MarkdownParser 
For test 481, the test that it gave an incorrect output for, the problem is that CommonMark expects a link here since it uses HTML link syntax but the MarkdownParser does not have code to account for this syntax and read it. So to solve this issue would require a lot more code to be added to account for HTML link syntax. 
![](givenCode1.PNG)
![](givenCode2.PNG)
![](givenCode3.PNG)
![](givenCode4.PNG)
<br/>
<br/>

### Our group MarkdownParser
For test 41, the problem with our parser is that it does not disregard a link if it has a space in the middle of it. This would probably require the addition of some if statement that could check if there is a space where the link should be. 

For test 481, the problem is similar to the given MarkdownParser because this parser does not account for HTML link syntax. So it would require a lot more code to be added to this parser. 
![](ourCode1.PNG)
![](ourCode2.PNG)