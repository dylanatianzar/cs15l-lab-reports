# Lab 2 Report
## Dylan Atianzar A17609722
## String Server Part 1
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

Everytime a link is input, the method handleRequest is called. Thus, all that is required as a parameter is the url link.

![Link](https://user-images.githubusercontent.com/69043855/215035170-30e3edd0-8e3e-4462-86a1-e58e25298630.png)
