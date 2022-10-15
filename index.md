# Lab Report Week 3

In this CSE 15L Week 3 lab report, I will summarize our learning progress in week 2 and week 3.

In Part 1, I will introduce a simple search engine that we built in class, which is inspired by the number server.

Functions include adding a string to the list, showing the full array list, and search for a certain string from the list.

In Part 2, I will go over our debugging process in week 3 lab, and explain the failure-inducing inputs, the symptoms, and the bugs.


## Part 1

```
public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Number: %d", num);
        } else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("count")) {
                    num += Integer.parseInt(parameters[1]);
                    return String.format("Number increased by %s! It's now %d", parameters[1], num);
                }
            }
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    arr.add(parameters[1]);
                    return String.format((parameters[1])+ " is added to the list! Current list: " + arr);
                }
            }
            if (url.getPath().contains("/search")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    String result = "";
                    for (String element : arr){
                        if (element.contains(parameters[1])){
                            result = result + " " + element;
                        }
                    }
                    return result;
                }
            }
            return "404 Not Found!";
        }
    }
}
```

Above is the code of the search engine.


![Image](./add%20banana.png)

Above is the ```add``` method. We are adding ```banana``` to the list.
I also showed that now we have ```apple```, ```pineapple```, ```banana``` in the list.

When we find ```/add``` in the path, we check the value of ```parameters[0]```, which is the string before ```=``` in the path.
If ```parameters[0]``` is ```s```, then we will add ```parameters[1]``` to the arraylist. In this case, ```parameters[1]``` is the input ```banana``` after the ```=``` in the path.
After adding ```parameters[1]``` to the list, we return on the webpage that ```parameters[1]``` is added to the list, and we will show the current list.

![Image](./search%20a.png)

Above is the ```search``` method. We are searching the string ```a``` from the list. The list currently contains ```apple```, ```pineapple```, ```banana```.

In the ```if``` statement, we use the String ```result``` to update the result value, and we use the String ```element``` to search in the arraylist and update the ```result```. When we find a string in the list that contains ```parameters[1]``` (the input in the path, which in this case is "a"), we update the ```result``` string by adding the ```element``` to the ```result```.

It turns out that all three words contain the string ```a```, so we update and return ```result``` as ```apple pineapple banana```, and we show them on the webpage.

![Image](./search%20apple.png)

Above is the ```search``` method. We are searching the string ```apple``` from the list. The list currently contains ```apple```, ```pineapple```, ```banana```.

In the ```if``` statement, we use the String ```result``` to update the result value, and we use the String ```element``` to search in the arraylist and update the ```result```. When we find a string in the list that contains ```parameters[1]``` (the input in the path, which in this case is "apple"), we update the ```result``` string by adding the ```element``` to the ```result```.

It turns out that ```apple``` and ```pineapple``` from the list contain the string "apple", so we update and return ```result``` as ```apple pineapple```, and we show them on the webpage.


## Part 2

### Bug 1 - filter

![Image](./code%20of%20the%20test1.jpeg)

Above is the failure-inducing input. The input is ```{"apple", "banana", "cheery", "dragon fruit", "eggplant"}```.

![Image](./bugcode1.png)

In this bug code above, the expected is ```banana```, but the actual is ```eggplant```.

![Image](./symptoms1.png)

Above is the symptom(output of the test).

The bug is causing this output because 

### Bug 2 - reversed

![Image](./the%20bug1.png)
In this bug code, the goal is to return the new array, but the code actually returned the old array. 

![Image](./Bug2.png)

[Lab Reports](https://github.com/fergusyyang/cse15l-lab-reports)

[Lab Report 0](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/week-0-lab.md)

[Lab Report 1](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/lab-report-1.md)
