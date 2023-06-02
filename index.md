# Debugging Scenario

## Post Written by a Student

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

Hello, I am currently using Mac OS and VS Code to code. Because I am a Mac OS user, I use zsh command line for terminal, which is a built-in terminal in VS Code.

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

![img](./Lab%209/error1.png)

![img](./Lab%209/test.png)
This is the test that failed.

![img](./Lab%209/method.png)
This is the method that causes a bug

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

The input of the test method in [Lab 3](https://github.com/ucsd-cse15l-w23/lab3) was an array of [1, 2, 3, 4, 5] I am expected to see the new array with reversed order of the original input array, which is [5, 4, 3, 2, 1]. However, I am getting this error message in the terminal when I am testing the method using JUnit. However, my code looks right. Please HELP ME.

## Response from the TA

### Analysis of the Terminal Output

The terminal indicates that the one of the elements of the expected and actual array are different. The element was expected to be 5 but the actual element is 0. Since your expected array indicates that the 5 is your 0th index, there is an unexpected output from 0th index.

### Analysis of the Code of Your Method

You created a new integer array. Then, you implemented the for loop (to my understanding) intended to traverse through the input array and assign the new array with values in reversed order. However, you are actually assigning values to the input array. In other words, your code is doing nothing to the new array that you created to store the reversed order values. Additionally, since your new array `newArray` is empty, the array only contains 0 because 0 is the default values. Therefore, your `arr`, the input array, will be an array with 0s in all indices.

### Debug

Since you should return the new array, according to the comment above your method. I would return the `newArray`, instead of `arr`.

![img](./Lab%209/step1.png)
This will return the `newArray`

Now, you should assign the values in `arr` to the `newArray` in the reversed order by doing this:
![img](./Lab%209/step2.png)

This way, each element in `newArray` is assigned to the corresponding element in `arr` in reversed order.

The bug is fixed!
![img](./Lab%209/fixed.png)

# Reflection

After the first Skill Demonstration, I thought that there would be nothing to learn in this course. However, I was definitely wrong: There are much more to learn and experience in this course, such as writing a bash commands in sh file and in java file and editing a file using Vim. In the labs, it was fun to explore and experience those unknown world of terminal implementation. Furthermore, the skills learned in this course will definitely be very helpful in my potential job or in my life of coding.
