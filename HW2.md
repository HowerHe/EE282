# Homework 2
## Questions
1. In your own directory (/$USER), create a directory with the name _trash_bin_1_. Then go into that directory, and create an   empty file named with _trash_ and a new directory named with _trash_bin_2_. Use a command to show what you have created.  
   Move the file you've just created into the directory _trash_bin_2_. You can use a command to make sure you have done things right.  
   Delete the file you’ve created. You can use a command to make sure you have made it.

2. Suppose you have a matrix _mymatrix_ and a dataframe _mydf_ in R. Compare the notation of `[...]` and `[[...]]`. Extract the first column of the matrix and the dataframe.

3. Write an empty script named with script_1 under the directory _my_script_. And change the permissions of that script so that it can be used by everyone. But only you have the permission to modify that script. Please use octal format to change the permissions.


## Answers
1. To change to your own directory, you can use `cd ~`. And `mkdir trash_bin_1` to make the first directory. Then use `cd trash_bin_1` followed by `touch trash` and `mkdir trash_bin_2`. To show what you have created, use `ls`.  
   To move the file, use`mv trash trash_bin_2`. You can use `ls` and `cd trash_bin_2` followed by `ls` to confirm your operations.  
   Just use `rm trash` and `ls`.

### Question 1 Comments:
FYI /$USER will probably almost never exist. if you want the user to go to their home directory, they would do as you have stated or cd $HOME, also you can skip having to cd into trash_bin_2 by just doing ls trash_bin_2/
Very nicely done.

2. `mymatrix[,1]` can be used to extract the first row of _mymatrix_. To extract the first row of the _mydf_, `mydf[[1]]` can be used. `mydf[1]` can also do the similar thing, but the result is still a dataframe. `mydf[[,1]]` cannot work since it doesn't include a range.

### Question 2 Comments:
Please re-attempt this question. You are attempting question 2 option 1 with numeric indices. Please ask a question relating two a dataframe and a matrix that both contain the same data. The question should ask how to access the **columns** (not rows as you've said in your answer) using numbers and various types of brackets. Please see the [question again](https://sites.google.com/uci.edu/fundamentals-of-informatics/syllabus/assignments/homeworkforweekofoctober11th).

3. 
```
mkdir my_script
chmod 711 my_script
cd my_script
touch script_1
chmod 755 script_1
```

### Question 3 Comments:
Very nicely done. I just suggest using 755 instead of 711 to the my_script folder or else users will not be able to list contents or see the contents of that directory, making your script_1 file inaccessible. I also recommend adding .sh to the end of your script filename. It makes it easier to do a quick search of scripts incase you need to find an old script or back them up using find . -name "*.sh" I recommend updating your readme answer to chmod 755 my_script
