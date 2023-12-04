# Lab Report 5

## Part 1 - Debugging Scenario
### Anonymous
**20 minutes ago**
<br>
Hello, I ran into a failure when running the command *bash test.sh* for Lab 7's file, ListExamples.java, and was not sure what the error could possibly be. Since I got 1 failure, I know that the bug is in my code and is not getting the expected output
and I was wondering if I could get some assistance with what the bug may be.
<br>
<img width="531" alt="Screenshot 2023-12-03 at 9 28 27 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/e69353a0-0ec5-4cc2-9945-53d82c566fec">
<img width="650" alt="Screenshot 2023-12-03 at 9 32 45 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/7816b2cb-0275-47ba-b52d-6e1ae949830a">
<img width="599" alt="Screenshot 2023-12-03 at 9 27 42 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/049fe676-b99d-40cb-a38e-e0dbae832bfe">
<img width="638" alt="Screenshot 2023-12-03 at 9 33 10 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/d30e3476-9e2f-429c-99af-51cbf41ce995">

### TA
**Just now**
<br>
Hello, if you look closely at the terminal error, it shows that there is an error just with testMerge2() meaning there may be an issue with the merge function. I would suggest looking closely at which index number is being
used as it is important for the code to run successfully.

**Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.**
<br>
<img width="419" alt="Screenshot 2023-12-03 at 9 41 41 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/cfdfe9b1-7849-4bde-984c-f7ac3bc68ddd">
<br>
<img width="284" alt="Screenshot 2023-12-03 at 9 42 23 PM" src="https://github.com/tumale/cse15l-lab-reports/assets/90641843/92027d12-0935-4760-827c-f9678a96225f">
<br>
It ran successfully because the index number was fixed from index1 to index2 which allows the list to be added to index2 respectively. 

## Part 2 - Reflection
In the second half of the quarter taking CSE 15L, I learned a lot about fixing and testing bugs and how to test them in a more convenient and concise manner. Building the autograder really 
helped with doing so and I was able to use it effectively. I also learned a lot about shortcuts with using bash and editting using vim and found them very interesting and fun to play around with.
