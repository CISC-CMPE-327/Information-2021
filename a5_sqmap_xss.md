
## SQL-Injection Security Report 

Before deployment, let's scan for SQL injection bugs and curate an injection vulnerability report, by following the steps below:

- Install [SQLmap](https://github.com/sqlmapproject/sqlmap) (git clone or download & unzip their zip/tar.gz file)
- Manually start your web application.
- Inside the sqlmap folder, you can run their python script through the command `python sqlmap.py -h` without errors.
- Scan your website by using `python sqlmap.py -u http://127.0.0.1:8081/ --forms --batch --crawl=10` 
- Save the log for use later.
- Manually login your website with a valid user account. 
- Check the your session id (let's refer it by `your_session_id`) in the cookie through the request headers of the index page (LocalHost or 127.0.0.1) in the browser. [How?](https://www.google.com/search?q=chrome+how+to+check+request+header&oq=chrome+how+to+check+request+header)
- Scan your website again by using `python sqlmap.py -u http://127.0.0.1:8081/ --forms --batch --crawl=10 --cookie=your_session_id` here `your_session_id` is the one you obtained from the last step.
- You should be able to see that it is scanning restricted forms that only available after login (i.e. authentication).
- Save the log for use later.

Now you have all the logs. Let's compile a SQL injection scanning report by filling a table following this format, then answer the questions below.

|      | Route/URL                      | Parameter | Number of Injection Trials | Number of Successful Trials |
|:----:|--------------------------------|:---------:|:--------------------------:|:---------------------------:|
| Scan | http://127.0.0.1:8081/register |   email   |             14             |             0               |
|      |                                |           |                            |                             |
|      |                                |           |                            |                             |

#### :book: Questions:

1. :ship: Are all the user input fileds in your application covered in all the test cases above? Any successful exploit?
2. :ship: We did two rounds of scanning. Why the results are different? What is the purpose of adding in the session id?
3. :ship: Summarize the injection payload used based on the logs, and breifly discuss the purpose. 


## XSS Security Report 

- Install [PwnXSS](https://github.com/pwn0sec/PwnXSS) (git clone or download & unzip their zip/tar.gz file)
- Manually start your application
- Inside the pwnxss folder, scan your web application by `python pwnxss.py -u http://127.0.0.1:8081/`
- Save the log for use later.
- Manually login your website with a valid user account. 
- Check the your session id (let's refer it by `your_session_id`) in the cookie through the request headers of the index page (LocalHost or 127.0.0.1) in the browser. [How?](https://www.google.com/search?q=chrome+how+to+check+request+header&oq=chrome+how+to+check+request+header)
- Scan your website again by using `python pwnxss.py -u http://127.0.0.1:8081/ --cookie='{"session":"your_session_id"}'` here `your_session_id` is the one you obtained from the last step.


Now you have all the logs. Let's compile a scanning report by filling a table following this format, then answer the questions below.

|      | Route/URL                      | Parameter | XSS successful? |
|:----:|--------------------------------|:---------:|:--------------------------:|
| Scan | http://127.0.0.1:8081/register |   password |             NO             | 
|      |                                |           |                            |  
|      |                                |           |                            |   

#### :book: Questions:

1. :ship: We did two rounds of scanning. Why the results are different? What is the purpose of adding in the session id?
1. :ship: Are all the possible XSS (script injection) links/routes covered in the table above? (think about any links that will render user inputs, such as URL paramer, cookies, flask flash calls). If not, are those link/pages vulnerable to XSS?
