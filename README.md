Download Link: https://assignmentchef.com/product/solved-program-that-prompts-the-user-to-enter-the-name-of-a-file
<br>
5/5 - (2 votes)

Write a program that prompts the user to enter the name of a file. The program finds the pairs of encoded/decoded words in the file.



Enter the file name: words.txt

words.txt contains

nwlxmnhellofleedklloamountfunctionprogramsearchjgnnqcrackdsbdlencodeshiftdecodekhoormessagedefendmnonwmclambcstring

Output: encode/decoded words are written to file: words.txt.sft

The program reads the content of the file and stores the words in an array of strings, the program then finds the pairs of encoded/decoded words and writes them to the output file.1. Name your program file_search.c. The output file name should be the same name as the input file but with an added extension of .sft. In this example, the original file name is words.txt. The output file name is then words.txt.sft. Assume the file name is no more than 100 characters. Assume the length of each line in the input file is no more than 100 characters. Assume the input file contains no more than 1000 words.

2. In the program, use the shift function (provided in shift.c) to help search for pairs of encoded/decoded words. The function shifts the alphabetical letters message in by shift_amount.

void shift(char *message, int shift_amount, char *shift_message){

for(; *message != ‘ ’; message++){if(*message = ‘a’ &amp;&amp; *message &lt;= ‘z’)*shift_message++ = (*message – ‘a’ + shift_amount)% 26 + ‘a’;else if(*message = ‘A’ &amp;&amp; *message &lt;= ‘Z’)*shift_message++ = (*message – ‘A’ + shift_amount)% 26 + ‘A’;else*shift_message++ = *message;}

*shift_message=’ ′;}

message is a string containing the word to be encoded, and shift_message is the string containing the word after being shifted by shift_amount. shift_amount represents the amount by which each letter in the message to be shifted, in the range of 0 to 25. Lower-case letters remain lower-case when shifted, and upper-case remain upper-case. For example, if the message is “make”, and shift_amount is 3, the function will assign shift_message by “pdnh”. If the message is “Jr”, and shift_amount is 23, the function will modify message to “Go”.Note: words in the file could be pairs of encoded/decoded of any shift amount in the range of 0-25