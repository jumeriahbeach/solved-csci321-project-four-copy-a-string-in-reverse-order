Download Link: https://assignmentchef.com/product/solved-csci321-project-four-copy-a-string-in-reverse-order
<br>
<strong>Objectives:</strong>

<ol>

 <li>Declare and initialize null-terminated string</li>

 <li>Apply indirect address</li>

 <li>Write loop</li>

 <li>Apply Irvine.inc library functions to display a string</li>

</ol>

<strong>Problem Description:</strong>

Write a program with a loop and indirect address that copies a string from source to target. Revising the character order in the process. Use the following variables:

source BYTE “This is the string that will be reversed”, 0

target BYTE SIZEOF source DUP(‘#’)

You may refer to the Programming Exercise #7 on Page 138 of the textbook.

<strong>Hint:</strong>

You may study the book example “Copying a String” on page 127 first. However, this project has three different things from the book’s example.

<ol>

 <li>You need two index register. One for the index of source, another for index of target. You can use Register ESI for index of source and Register EDI for index of target</li>

 <li>You will not copy the last character in source, which is null character (the terminator of source string). So the initial value of ESI shall be set as OFFSET target – 2 since the target string is stored right after the source string in memory</li>

 <li>After the loop, you need add null character to the end of the target string</li>

</ol>

<strong>How to View Output:</strong>

After Chapter Five, you will be able to write statement to print out the output on screen. So far, you need to see output in memory. After your project can be assembled and run successfully, you may do following things:

<ol>

 <li>Click on the grey bar located on the left of side of the “invoke ExitProcess, 0” statement to set up the Break Point</li>

 <li>Go to Debug and click on Start Debugging</li>

 <li>Go to Debug -&gt; Windows -&gt; Memory -&gt; Memory 1 (or: ALT + 6). You will see a window on the right side of your code. Type 0x004068D0 in Address field and you will see the following window (next page). If you don’t see the source string, then your computer may store .data section in difference memory location. You may need to search to find it. If you see the source string but the string after it is not a reverse of source string, then your program has logic errors.</li>

 <li>After check the result, press F10 to continue and finish the program execution.</li>

</ol>