# how i solved it

## first thoughts- Extracting sequences from files into a list of strings 
I figured that a good divider is the ">" sign and thats what ill be using to create the proper sequences.<br>
at first i thought that would be enough but after looking at the "complicated" text file i decided to add<br>
a Bool to check if the previous line was a separator and in the case make a new string otherwise add to previous line<br>

After testing around i realised i dont really need to use the bool and insted append the list each time we reach the ">" sign <br>
so each time i append the list the string that has been acumulating between signs then resetting the string to ""<br>
Then the output looked kind of weird and i thought i had more than 4 indexes in the list but a len(ls) output 4 <br>
so i figured its something else. i decided to strip each string thus removing the whitespace and to my satisfaction <br>
there was a match between the sequences and my output from  looping through my list <br>
also realised there are letters in the sequence that shouldnt be counted but my inital thought is to handle that in the counting later <br>



