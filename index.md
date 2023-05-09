# Interesting Implementations of grep Command

## -c Flag

```
grep -c "word" filename
```

This line of command counts the occurence of the `word` in the file.

```
grep -c "9/11" technical/911report/chapter-1.txt
```

This line of command counts the occurence of the `9/11` in the `chapter-1.txt` in the `technical/911report/` directory. The output of this command is:

![Image](./Lab5//FInd%20Word%20Single.png)

```
rep -c "9/11" technical/911report/*.txt
```

This line of command counts the occurence of the `9/11` in all of the text files in the 911report directory and show the occurence of the word in each txt file. The output of this command is:

![image](./Lab5/Screenshot%202023-05-08%20at%2021.28.49.png)

## -n Flag

```
grep -n "word" filename
```

This line of command shows the number of line where the `word` given as input exists in the file of the `filename`.

```
grep -n "study" technical/biomed/1468-6708-3-1.txt
```

The command above finds the word `study` in the `1468-6708-3-1.txt` file in the `technical/biomed/` directory and shows the line number where the word occurs in that file.

![image](./Lab5/Line%20Number%20Singular.png)
