# How I Solved It

## 🧠 First Thoughts – Extracting Sequences from Files into a List of Strings  

I figured that a good divider is the `">"` sign, and that’s what I decided to use to create the proper sequences.  
At first, I thought that would be enough, but after looking at the "complicated" text file, I decided to add a **boolean flag** to check if the previous line was a separator. If it was, I would create a new string; otherwise, I would add to the previous line.  

After testing, I realized I didn’t actually need the boolean flag. Instead, I could simply **append the list each time we reach a `">"` sign**.  
Each time I appended, the accumulating string between separators would be stored, and then I reset the string to `""`.  

The output initially looked strange—I thought I had more than four indexes in the list, but `len(ls)` returned **4**.  
So, I figured something else was off. I then decided to **strip each string**, removing unnecessary whitespace. To my satisfaction, this produced a **perfect match** between the sequences and my output when looping through my list.  

I also noticed that **some letters in the sequences shouldn’t be counted**, but I decided to handle that later during the counting phase.  

After finishing the **counting process**, I created a **list of dictionaries** and learned the basics of **Matplotlib**.  
I considered breaking the assignment into functions, but since it's such a **small program**, I didn’t see much point.  
If the program could handle the "complicated" file, it could handle the simple one as well.  

However, **if I were to use functions**, I would structure it as follows:  
- A function that **takes a string and converts it into a list of sequences**.  
- A function that **counts occurrences and returns a list of dictionaries**.  
- A function to **handle graph output**, possibly with `**kwargs` to customize the visualization.  

---

## 🔄 Update:  
I **realized the assignment required functions**, so I quickly refactored the code to use a **function with `filepath` as a parameter**.  
