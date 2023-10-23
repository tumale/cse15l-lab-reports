# Lab Report 2

## Part 1

**StringServer.java code**
```

import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
import java.util.List;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    List<String> message = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Add a message!");
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    message.add(parameters[1]);
                    String output = "";
                    for (int i = 0; i < message.size(); i++) {
                        output = output + message.get(i) + "\n";
                    }
                    return String.format("%s", output);
                }
            }
            return "404 Not Found!";
        }
    }
}
class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}

```

**Using /add-message**
<br>
Screenshot 1:
<img width="1211" alt="Screenshot 2023-10-22 at 7 42 51 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/527e2557-f325-45ba-a9b3-8572d1b15baf">
The getPath() method was called which contains /add-messages. The getQuery() method was also called in order to add the message in the query of the URL. This allowed for number values to show up in the output in the string.
<br>

<br>
Screenshot 2:
<img width="1215" alt="Screenshot 2023-10-22 at 7 43 16 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/56a0cf8f-bdb9-486a-ada3-3403c2729408">
The getPath() method was called which contains /add-messages. The getQuery() method was also called in order to add the message in the query of the URL. This allowed for a link to be added and printed out in the output following the previous message.

## Part 2
**The path to the private key for your SSH key for logging into ieng6**
<br>
<img width="342" alt="Screenshot 2023-10-22 at 8 01 58 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/d75386b8-e710-4acb-803b-e272f7c48958">

**The path to the public key for your SSH key for logging into ieng6**
<br>
<img width="276" alt="Screenshot 2023-10-22 at 8 21 25 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/41d10148-364d-4391-b0b6-b85d24401642">


**A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password**
<br>
<img width="765" alt="Screenshot 2023-10-22 at 8 18 27 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/f122a3fc-9290-4f6c-be9b-62054ce8fa32">
<img width="363" alt="Screenshot 2023-10-22 at 8 18 49 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/6be72e26-e778-4cf3-8691-09c2ed8f6093">

## Part 3
During week 2 and week 3, I learned a lot of new things that I did not know before. I learned that you are able to connect remotely with other students and are able to see their outputs. I also learned about logging in to my own account without the use of a password, which I did not know before.
