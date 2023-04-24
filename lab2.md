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
## Examples of /add-message working as intended:


![Image](https://user-images.githubusercontent.com/58676663/233942503-8500772e-1aa3-484b-8a3d-2921e551d50b.png)
![Image](https://user-images.githubusercontent.com/58676663/233942827-7bcb3c39-cb38-4669-b565-a58b59b91936.png)

### Screenshot 1:
- The handleRequest method of the StringHandler class is called.
- The relevant argument to the handleRequest method is a URI object representing the URL of the request. The value of the URI object is http://localhost:8080/add-message?s=Hello@20World, where localhost is the hostname, 8080 is the port number, /add-message is the path, and s="Hello World!" is the query -parameter.
- The message field of the StringHandler class is updated with the value "Hello World!" appended to the existing message string. The updated value of the message field is returned as the response.

### Screenshot 2:
- The handleRequest method of the StringHandler class is called.
- The relevant argument to the handleRequest method is a URI object representing the URL of the request. The value of the URI object is http://localhost:8080/add-message?s=My@20Name@20is@20Gautham@20Kishore, where localhost is the hostname, 8080 is the port number, /add-message is the path, and s="My Name is Gautham Kishore" is the query -parameter.
- The message field of the StringHandler class is updated with the value "My Name is Gautham Kishore" appended to the existing message string. The updated value of the message field is returned as the response.



## Part 2: Debugging and Analyzing Tests

### A failure-inducing input for the buggy program:
```java
    @Test
  public void testReverseInPlace2() {
    int[] input1 = new int[]{ 1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);

    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
  } 
```

### An input that doesn’t induce a failure:
```java
@Test
  public void testReverseInPlace3() {
    int[] input1 = new int[]{ 1};
    ArrayExamples.reverseInPlace(input1);

    assertArrayEquals(new int[]{1}, input1);
  }
```
### Image of Terminal Output of Failed Test
![Image](https://user-images.githubusercontent.com/58676663/234128409-6efde721-cafe-436a-880d-2519dd4985eb.png)


### Original Implementation(Buggy)
```java
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
### Fixed Implementation(Passes Tests)
```java
static void reverseInPlace(int[] arr) {
    if(arr.length < 2 || arr == null) { return; }

    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```
