# Lab Report 2

## Part 1

**StringServer.java code**
'''
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
'''

**Using /add-message**
<img width="1280" alt="Screenshot 2023-10-22 at 7 23 11 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/e5e8080f-694e-4d2c-9c84-251fa73df7d6">
<img width="1278" alt="Screenshot 2023-10-22 at 7 23 43 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/cf5315f0-f4f0-4ae2-a24c-78e13fa39b02">
