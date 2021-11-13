# Testing for SQL Injection:

For this sprint, we will run fuzzy test against our backend APIs to check for sql injections.
There are many injection payload we can test, some of them are database-specific. 
For this sprint, we will use general injection payload for testing. You can find the file from [here](https://raw.githubusercontent.com/payloadbox/sql-injection-payload-list/master/Intruder/detect/Generic_SQLI.txt). We will test the **register function** and the **create product function**.

For each function, following the steps below:
- Create a test case for each parameter of that function
- For each test case, assuming that the other parameters are correctly following the specification.
- Read all the payloads from the given file above. 
- Going through each line (each payload), and test run the function with the payload as the value for the chosen parameter.
- Check if there is any exceptions thrown by the function.
  - Make sure that you don't have a universal try..catch:.. statement in the function being tested



