# Interesting Implementations of grep Command

## -c Flag

### Definition

```
grep -c "word" filename
```

This line of command counts the occurence of the `word` in the file.

### Example 1

```
grep -c "9/11" technical/911report/chapter-1.txt
```

This line of command counts the occurence of the `9/11` in the `chapter-1.txt` in the `technical/911report/` directory. The output of this command is:

![Image](./Lab5//FInd%20Word%20Single.png)

### Example 2

```
rep -c "9/11" technical/911report/*.txt
```

This line of command counts the occurence of the `9/11` in all of the text files in the 911report directory and show the occurence of the word in each txt file. The output of this command is:

![image](./Lab5/Screenshot%202023-05-08%20at%2021.28.49.png)

## -n Flag

### Definition

```
grep -n "word" filename
```

This line of command shows the number of line where the `word` given as input exists in the file of the `filename`.

### Example 1

```
grep -n "study" technical/biomed/1468-6708-3-1.txt
```

The command above finds the word `study` in the `1468-6708-3-1.txt` file in the `technical/biomed/` directory and shows the line number where the word occurs in that file.

![image](./Lab5/Line%20Number%20Singular.png)

### Example 2

```
grep -n "RIPA" technical/biomed/*.txt
```

The command above finds the word `"RIPA"` in all the text files in the `technical/biomed/` directory and shows the line number where the word occurs in each file.

![image](./Lab5/Line%20Number%20Multiple.png)

## -r Flag

### Definition

```
grep -r "word" directory
```

This line of command searches for the word in all files in the directory and its subdirectories recursively.

### Example 1

```
grep -r "RIPA" technical/biomed/
```

This command looks for the word "RIPA" in all the files in the `technical/biomed/` directory recursively and prints all the directories that contains the word.

![image](./Lab5/Recursive%201.png)

### Example 2

```
stringsearch-data % grep -r "Jewish" technical
```

This command looks for the word "Jewish" in all the files in all the subdirectories in the `/technical/` directory and prints all the directories where the word occurs.

![image](./Lab5/Recursive%202.png)

## -C Flag with number

### Definition

```
grep -C <n> "word" filename
```

This command prints n number of lines before and after the line where the word occurs in the filename.

### Example 1

```
grep -C 5 "Jewish" technical/biomed/\*.txt

```

The command looks for the word "Jewish" in all the text files in the `technical/biomed/` directory and then prints 5 lines before and after the word occurs in the text file.

![image](./Lab5/five%20lines.png)

### Example 2

```
grep -C 5 "F-15" technical/911report/chapter-1.txt
```

This command finds the word "F-15" in a `technical/911report/chapter-1.txt` file and prints 5 lines after and before the line where the word occurs.

![image](./Lab5//Five%20Lines%20in%20Single%20File.png)

# Work Cited

## Chat GPT

The prompt that I gave to Chat GPT:

> What are some interesting commands using grep command?

Then, ChatGPT gave me this response:

Grep is a powerful command-line tool used for searching plain text files for specific patterns. Here are some interesting commands using grep:

1. Search for a word in a file:

   ```
   grep "word" filename
   ```

2. Search for a word in multiple files:

   ```
   grep "word" file1 file2 file3
   ```

3. Search for a word in all files in a directory and its subdirectories:

   ```
   grep -r "word" directory
   ```

4. Search for a word in all files with a certain file extension:

   ```
   grep "word" *.txt
   ```

5. Search for a word but ignore the case:

   ```
   grep -i "word" filename
   ```

6. Search for a word and show the line number where it occurs:

   ```
   grep -n "word" filename
   ```

7. Search for a word and show the lines before and after it:

   ```
   grep -C 3 "word" filename
   ```

8. Search for a word and count the number of occurrences:

   ```
   grep -c "word" filename
   ```

9. Search for lines that match a regular expression pattern:

   ```
   grep "pattern" filename
   ```

10. Search for lines that do not match a regular expression pattern:

```
grep -v "pattern" filename
```

I chose three interesting implementation examples of `grep` from the response. Additionally, I did not regenerate response from Chat GPT after this prompt.
