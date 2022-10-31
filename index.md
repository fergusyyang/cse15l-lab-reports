# Lab Report Week 5

In this week 5 lab report, I will give 9 command-line examples and explain how I used them.
In example 1 to 3, I will introduce how to use ```find``` in the simplest way: to use it directly and list all the files in the directory.
In example 4 to 6, I will explain how to use ```find some-files -name``` to look for a file in the directory given a specific name.
In example 7 to 9, I will explain how to use ```find``` with ```xargs wc``` to find and count the lines/words/characters of the files in the given directory.


## Example 1
In the first example, we used the command ```find``` in the simplest way. We wrote ```find technical/``` on the command line. The ```find``` command can list all the files in the directory. In this case, we are listing the files in the technical directory.
![Image](./1findtech%20input.png)
![Image](./1%20find%20technical.png)


## Example 2
We want to use ```find``` in two different directories together, so we wrote ```find technical/ lib/``` to list all the files in both of these directories.
![Image](./2%20tech%20and%20lib.png)
![Image](./2tech%20and%20lib%20output.png)

## Example 3
We can use ```find``` with a path. For example, ```find technical/911report```. Then the command would list all the files in the ```911report``` directory.
![Image](./3%20find%20technical%20911.png)


## Example 4
Using ```find``` with ```-name```, we can find certain files that meets our criteria. For example, we want to list the files with ```.txt``` in the directory. We write ```find technical -name "*.txt"``` so the sommand will list all files in ```technical``` directory that are ```.txt``` files.
![Image](./4-name%20input.png)
![Image](./4-name%20output.png)

## Example 5
Similar to example 4, we can write ```find technical -name "chapter-12.txt"``` to find and list the file ```chapter-12.txt``` if it is in the ```technical``` directory.
![Image](./5-name%20chapter12.png)

## Example 6
Similar to example 4, we can write ```find technical -name "*2.txt"``` to list the files that ends with "2.txt" in the ```technical``` directory.
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
