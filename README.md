Download Link: https://assignmentchef.com/product/solved-cpe-325-assignment-8
<br>
<h2>Assignment</h2>

<ol>

 <li>Implement the following functions in C:</li>

</ol>

<table width="594">

 <tbody>

  <tr>

   <td width="277">void UART_initialize();</td>

   <td width="317">Configures UCI to work in the UART mode at the baud rate as follows: if your first name hasan even number of letters use 19200, otherwise use 115200.</td>

  </tr>

  <tr>

   <td width="277">voidUART_sendCharacter(char c);</td>

   <td width="317">Sends a character via UART</td>

  </tr>

  <tr>

   <td width="277">char UART_getCharacter();</td>

   <td width="317">Waits for a character from UART and returns it.</td>

  </tr>

  <tr>

   <td width="277">void UART_sendString(char* string);</td>

   <td width="317">Sends a string via UART usingsendCharacter(char c)</td>

  </tr>

  <tr>

   <td width="277">void UART_getLine(char* buffer, int limit);</td>

   <td width="317">Receives characters via UART usingUART_getCharacter()until it finds the new line character or until the limit of characters is exceeded. Writes that string (excluding the new line character) to the buffer allocated outside of the function.Terminates the string with the null character.</td>

  </tr>

 </tbody>

</table>

Test your functions to make sure they work properly and none of them writes or reads nonallocated memory. Make sure that UART_getLine() inserts the null character at the end of your string, and does not exceed the limit, including the null character.

<ol start="2">

 <li>Write a chat bot using functions from the previous part. When the user types “Hey, Bot!” and hits Enter, the bot greets the user and asks for their age. After age is entered, chat bot replies: “You are so young! I am 1&lt;x&gt; years old!”, where &lt;x&gt; is the age of the user. If the user enters 1000, the bot should reply “This cannot be true!”. Make sure each message in the chat starts from a new line. Specify author of each message as it is shown on the screenshot below (colored names are necessary for bonus part only):</li>

</ol>

<strong>Notes: </strong>

<ul>

 <li>You can use <a href="http://www.cplusplus.com/reference/cstdio/snprintf/">snprintf</a> function to concatenate strings, but make sure you do not overflow any buffers.</li>

 <li>The bot should be ready to reply to the “Hey, Bot!” message again without resetting the board.</li>

 <li>Use <a href="http://www.cplusplus.com/reference/cstring/strcmp/">strcmp</a> function to compare strings.</li>

 <li>Echo characters back if you want to see what you type.</li>

 <li>Use r
 sequence to properly start a new line.</li>

</ul>

<ol start="3">

 <li><strong> </strong>If the user has not communicated with your chat bot for longer than 15 seconds, the chatbot should send “Is anybody here?” to the terminal and repeat that message every 15 seconds until the user replies. Messages from the user should reset the wait time.</li>

 <li><strong>[ </strong>Use different <a href="https://misc.flogisoft.com/bash/tip_colors_and_formatting">colors</a> for the names of authors.</li>

</ol>

<h2></h2>