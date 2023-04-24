# Lab Report 2 - Servers and Bugs (Week 3)

## Part 1: StringServer Implementation
```java
import java.io.IOException;
import java.net.URI;

class StringHandler implements URLHandler {
// The one bit of state on the server: a string that will be concatenated by
// various requests.
String message = "";


public String handleRequest(URI url) {
    if (url.getPath().equals("/add-message")) {
        String[] parameters = url.getQuery().split("=");
        if (parameters.length == 2 && parameters[0].equals("s")) {
            String newMessage = parameters[1];
            message += "\n" + newMessage;
            return message;
        } else {
            return "400 Bad Request";
        }
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
## Examples of /add-message working as intended

![Image](https://user-images.githubusercontent.com/58676663/233942503-8500772e-1aa3-484b-8a3d-2921e551d50b.png)







