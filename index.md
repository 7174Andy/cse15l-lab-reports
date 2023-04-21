# Part 1

This is how I created `StringServer` webpage.

First I had to copy and paste the `Server.java` file from lab 2 Github repository. Then, I had to compile the `Server.java` file before compiling `StringSever.java`. 

The code below is what I wrote for the `StringServer.java`. 

```
import java.io.IOException;
import java.net.URI;

class StringHandler implements URLHandler {
    String message = "";

    public String handleRequest(URI url) {
        System.out.println(url);
        if (url.getPath().equals("/")) {
            return "Andrew Park's Homepage";
        } else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                message += parameters[1];
                message += "\n";
            }
            return message;
        } else {
            return "404 Not Found";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new StringHandler());
    }
}
```

## Images of the Webpage
![Image](./Lab3/First.png)

### Start Method
When the website is started, the main method in the StringServer class, and the main method takes in an array of string values of our argument in the terminal. Then the `start` method in the `Server` class is initiated in order to activate the server. This method takes in the integer value of the port number ranging from 1024 to 49151. 

