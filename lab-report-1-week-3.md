# Lab-report week 3

## Part 1 SearchEngine
- Creat the "SearchEngine.java" file, which can add the new string to the list, also can search the word being added. (like a dictionary)

- Write the code
```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Search implements URLHandler {
    ArrayList<String> arrlst = new ArrayList<String>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "Word List : " + arrlst.toString();
        } else if (url.getPath().contains("/add")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                arrlst.add(parameters[1]);
                return String.format("A new string (%s) is Added! There are %d strings in the word list", parameters[1],
                        arrlst.size());
            }
        } else if (url.getPath().contains("/search")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                ArrayList<String> results = new ArrayList<>();
                for (String ele : arrlst) {
                    if (ele.contains(parameters[1])) {
                        results.add(ele);
                        System.out.println(ele);
                    }
                }
                return "reuslt:" + results.toString();
            }
        } else {
            return "404 Not Found!";
        }
        return "404 Not Found!";
    }
}

class SearchEngine {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Search());
    }
}
```

- After you finish your code, you should compile and run it in the terminal, getting the URL website.
- Then, try your code on your browser.

 
- Firstly, we call the method "handleRequest" method, the "/add" if statement branches.
- The value of relevant field here is the url with the type URI, directed by the keyword "s=".
- The value here will add the "anewstringtoadd" string to the word list.
![addnewstring](https://user-images.githubusercontent.com/106074396/195793272-38942c55-b528-4e2f-b853-55c2b79e8aec.png)

- Secondly, we also call the method "handleRequest" method, the "/add" if statement branches.
- The value of relevant field here is the url with the type URI, directed by the keyword "s=".
- The value here will add the "pineapple" string to the word list.
![addpineapple](https://user-images.githubusercontent.com/106074396/195792907-745a3adf-03ce-4f5d-a2d1-ca4600a373a6.png)

- Thirdly, we also call the method "handleRequest" method, the "/add" if statement branches.
- The value of relevant field here is the url with the type URI, directed  by the keyword "s=".
- The value here will add the "apple" string to the word list.
![addapple](https://user-images.githubusercontent.com/106074396/195793577-aaba096f-10df-4d8c-9978-22cd1ce27215.png)

- Forthly, we also call the method "handleRequest" method.
- The value of relevant field here is the url with the type URI, directed by the keyword "s=", here we serached the word included "app".
- The values will not change. 
![search](https://user-images.githubusercontent.com/106074396/195793808-345203a7-4b7d-490b-843b-80b55702f337.png)


## Part 2 Bugs
## The first bug
![testreverse](https://user-images.githubusercontent.com/106074396/195951234-9f484228-f01c-44f9-aac3-6016666bcc76.png)

![symptomreverse](https://user-images.githubusercontent.com/106074396/195951313-ba5762ec-cd94-4e33-b699-fa341e8e0d24.png)


![bugfixed](https://user-images.githubusercontent.com/106074396/195953190-b7d713aa-9b11-4f1c-934b-3b5da7a57088.png)

- The sympton is "arrays first differed at element[2]; expected:<2> but was:<4>"
The connection between the symptom and the bug for the code is that it changed the arraylist lively. When it copyed the second half of the arraylist, it will copy the second half of the original arraylist for two times. 
- For this particular input, according to the bugs the return value will be {5,4,4,5}, but actually we expected the value {5,4,2,3}. Therefore, when we check the array. The first different output in this array is the the third one.

## The second bug
![test](https://user-images.githubusercontent.com/106074396/195956247-de6b4d82-f7d4-440d-9abc-53bf7c5b9f95.png)

![image](https://user-images.githubusercontent.com/106074396/195954926-54f7f710-4f7c-44f3-a742-a1f3aa4ed5b4.png)

![image](https://user-images.githubusercontent.com/106074396/195955087-8cee7bad-206b-41b6-8bac-1d02f3deb7bc.png)

- The sympton here is "java.lang.AssertionError: expected:<true> but was:<false>". The connection between symptom and the bug is that we expected the array "answer" is equal to the array "ListExamples.filer(input23,sc)". Since both fo the input I had are "sd" and "abf", which length is less than 5, it should be filtered through the checkString. 

- The reason why bug cause the particular symptom for this input is that we expected the result list should be["sd","abf"], but the bug code will run the result to be["abf","sd"]. Since the "result.add(0,s)" will add the new things at the front of the list, which cause the bugs happenned. 
