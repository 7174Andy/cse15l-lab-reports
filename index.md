# Interesting Implementations of grep Command

## -c Flag

```
grep -c "word" filename
```

This line of command counts the occurence of the `word` in the file.

```
grep -c "9/11" technical/911report/chapter-1.txt
```

This line of command counts the occurence of the `9/11` in the chapter-1.txt. The output of this command is:

![Image](./Lab5//FInd%20Word%20Single.png)

```
rep -c "9/11" technical/911report/*.txt
```

This line of command counts the occurence of the `9/11` in all of the text files in the 911report directory and show the occurence of the word in each txt file. The output of this command is:

![image](./Lab5/Screenshot%202023-05-08%20at%2021.28.49.png)
