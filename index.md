# Lab Report Week 5

In this week 5 lab report, I will give 9 command-line examples and explain how I used them.
In example 1 to 3, I will introduce how to use ```find -path```, to find all the paths that contains a given string.
In example 4 to 6, I will explain how to use ```find some-files -name``` to look for a file in the directory given a specific name.
In example 7 to 9, I will explain how to use ```find``` with ```xargs wc``` to find and count the lines/words/characters of the files in the given directory.


## Example 1
In the first example, we use the command ```find -path``` in the docsearch-main directory.

```find technical -path "*.txt"```
```
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/preface.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```
This command will find all path in the technical directory that ends with ```.txt```


## Example 2
In the second example, we are using ```find -path``` in the docsearch-main directory.

```find technical -path "*911report*"```
```
technical/911report
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/preface.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```

This will find all the paths that contains the string ```911report```

## Example 3
In the third example, we want to use ```find -path``` in the technical directory.

```find 911report -path "*chapter*"```
```
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```

This will find all the paths that contain the string ```chapter```.

## Example 4
Using ```find``` with ```-name```, we can find certain files that meets our criteria. For example, we want to list the files with ```.txt``` in the directory. We write ```find technical -name "*.txt"``` so the sommand will list all files in ```technical``` directory that are ```.txt``` files.
![Image](./4-name%20input.png)
![Image](./4-name%20output.png)

## Example 5
Similar to example 4, we can write ```find technical -name "chapter-12.txt"``` to find and list the file ```chapter-12.txt``` if it is in the ```technical``` directory.
![Image](./5-name%20chapter12.png)

## Example 6
Similar to example 4, we can write ```find technical -name "*2.txt"``` to list the files that ends with ```2.txt``` in the ```technical``` directory.
![Image](./6%202txt%20input.png)
![Image](./6%202txt%20output.png)

## Example 7
We use ```xargs wc``` to count the lines/words/characters of the files. For example, if we type in ```find technical|xargs wc```, then the command will count the lines/words/characters of all the files in the ```technical``` directory.
![Image](./7wc%20input.png)
![Image](./7wc%20output.png)

## Example 8
Similar to example 7, if we type in ```find technical/911report|xargs wc```, then the command will help us count the lines/words/characters for each files in the ```911report``` directory.
![Image](./8wc911%20input.png)
![Image](./8wc911%20output.png)

## Example 9
Similar to example 7, if we type in ```find technical/911report/*.txt|xargs wc```, then the command will count the lines/words/characters for all files in the ```911report``` directory that ends with ```.txt```.
![Image](./9wctxt%20input.png)
![Image](./9wctxt%20output.png)



[Lab Reports](https://github.com/fergusyyang/cse15l-lab-reports)

[Lab Report 0](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/week-0-lab.md)

[Lab Report 1](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/lab-report-1.md)

[Lab Report 2](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/week3-lab.md)
