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

finnished the counting process and created the list of dictionaries aswell as learnt the basics of matplot lib.<br>
considered breaking this asignment into functions in the end but since its such a small program i felt that there wouldnt be a point to it<br>
since if my program can handle the "complicated" one it will handle the simple one aswell<br>
but if i were to create functions i would create one that takes a string and converts its to  a list of sequeces<br>
another one that would count and return a list of dictionaries containing the informations<br>
and a third one to handle the output of the graph with perhaps **kwargs that could alter the output <br>

---
## Update:
realised asignment was supposed to be in a function format so i quickly updated and made it a function with filepath as parameter

