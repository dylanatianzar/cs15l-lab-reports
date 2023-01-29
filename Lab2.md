# Lab 2 Report
## Dylan Atianzar A17609722
## Part 1: String Server
This is the code for my String server.
```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler{
    String wholeList = "";

    public String handleRequest(URI url){
        if (url.getQuery() == null) {
            return "Add a message to string with /add-message path";
        }
        String[] parameters = url.getQuery().split("=");
        if (url.getPath().contains("/add-message") && 
                parameters[0].equals("s")){
            wholeList += parameters[1] + "\n";
            return wholeList;
        }
        return "404 not found!";
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException{
        if (args.length == 0) {
            System.out.println("Missing Port Number!");
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```
![Link](https://user-images.githubusercontent.com/69043855/215021280-2d4a44c2-c30f-4b4b-b755-777c8ed8ddbd.png)

Whenever a URL is sent to the domain that the server is running on, the method handleRequest is called. All that is required as an argument is the url link, which is given when the domain is accessed. This is the URI value. The wholeList variable is an empty string. As shown in the screenshot, when the path is `/add-message?s=[value]` the wholeList variable will add the value from the query and display it on the page. 

![Link](https://user-images.githubusercontent.com/69043855/215035170-30e3edd0-8e3e-4462-86a1-e58e25298630.png)
Upon the second call to `/add-message`, the method call is the same as the first screenshot which calls handleRequest. The URI url and wholeList values are relevant to this likewise. For both screenshots, the port int is an important part as well in order to access the web server. The url value changes with what the query is, and the value portion of the query is added to the wholeList string. Then, wholeList is displayed on the web page.

## Part 2: Bugs
The failure-inducing input for ArrayExamples.java: `int[] custom1 = {1,2,3,4,5}`
As a JUnit test and associated code: 
```
@Test
public void testReversed() {
    int[] custom1 = {1,2,3,4,5};
    assertArrayEquals(new int[]{5,4,3,2,1}, ArrayExamples.reversed(custom1));
}
```
An input that doesn't produce a failure: `int[] input1 = { }`
As a JUnit test and associated code:
```
@Test
public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
```

The output of both tests described above:
![Link](https://user-images.githubusercontent.com/69043855/215305087-8cdb5ea6-dfdc-4f62-95c3-07b24c923637.png)

Bug pre-fix:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
}
```

Bug post-fix:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```

The issue with the code was that the original array was being replaced by the new array which was empty. It would also the old array whose values became empty as a result of the replacement. The fix made it so that the new array would be filled by backwards of the old array and returns this new array. The result is that the array becomes correctly reversed.

## Part 3: What Did I Learn
From Week 2, I learned how to create a very basic web server. I never understood the importance of the port number or how the url can be manipulated through code; more importantly, the separate port numbers. My partner didn't understand why we couldn't use the same port number when we connected to the `ieng6` server. I explained it to my partner in that a port number would be like two separate boxes in the same room. If one box is full, then you can't continue to use that box, you would you have to use the other one. Additionally, the instance variables can be manipulated through multiple users given that the server is running.
