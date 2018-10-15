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


2. `mymatrix[,1]` can be used to extract the first row of _mymatrix_. To extract the first row of the _mydf_, `mydf[[1]]` can be used. `mydf[1]` can also do the similar thing, but the result is still a dataframe. `mydf[[,1]]` cannot work since it doesn't include a range.

3. 
```
mkdir my_script
chmod 711 my_script
cd my_script
touch script_1
chmod 755 script_1
```
