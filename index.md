# Lab Report Week 3

``

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

``

This is the code of the search engine.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/add%20banana.png)
This is the add method that we are adding banana to the list.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/search%20a.png)
This is the search method that we are searching "a" from the list.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/search%20apple.png)
This is the search method that we are searching "apple" from the list.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/the%20bug1.png)
In this bug code, the goal is to return the new array, but the code actually returned the old array. 

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/symptoms1.png)
This is the symptom(output of the test)

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/code%20of%20the%20test1.jpeg)
This is the code of the test.

[Lab Reports](https://github.com/fergusyyang/cse15l-lab-reports)

[Lab Report 0](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/week-0-lab.md)

[Lab Report 1](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/lab-report-1.md)
