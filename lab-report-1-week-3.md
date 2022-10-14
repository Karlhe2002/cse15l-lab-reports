# Lab-report week 3

## SearchEngine
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

 
- Firstly, we call the method "handleRequest" method.
![addnewstring](https://user-images.githubusercontent.com/106074396/195793272-38942c55-b528-4e2f-b853-55c2b79e8aec.png)

- Secondly, we also call the method "handleRequest" method.
![addpineapple](https://user-images.githubusercontent.com/106074396/195792907-745a3adf-03ce-4f5d-a2d1-ca4600a373a6.png)

- Thirdly, we also call the method "handleRequest" method.
![addapple](https://user-images.githubusercontent.com/106074396/195793577-aaba096f-10df-4d8c-9978-22cd1ce27215.png)

- Forthly, we also call the method "handleRequest" method.
![search](https://user-images.githubusercontent.com/106074396/195793808-345203a7-4b7d-490b-843b-80b55702f337.png)

Which methods in your code are called

What the values of the relevant arguments to those methods are, and the values of any relevant fields of the class

If those values change, how they change by the time the request is done processing
