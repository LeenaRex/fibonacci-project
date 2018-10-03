<b>RESTful web service to generate Fibonacci numbers</b><br/>
This project provides a RESTful web service to accept a number and return the first sequence of fibonacci numbers up to the count of the input number. For example, if the number 10 is entered the result will be the sequence of first 10 fibonacci numbers [0,1,1,2,3,5,8,13,21,34].
The HTTP method GET is used to fetch the result from the server, and the POST method is used to submit the request from the webpage form to the server.

<b>Getting Started</b><br/>
The project source code and dependent files are in GitHub:<br/>
<a href="https://github.com/leena-rex/fibonacci-project">https://github.com/leena-rex/fibonacci-project</a>

1. Download the project as a zip file to the desktop.
2. NodeJS and GIT needs to be already installed in the computer.
3. Extract the files from fibonacci-project.zip. 
4. In the Git Bash command-line prompt navigate to 'RestApiWebService' project folder. 
5. Important: Type: 'npm install' without the single quotes. This will install the dependent modules
   listed in the project's package.json file
6. Start the server with the following command:<br/>
   $> node app.js<br/>
   The server will start 'Listening on port 3000'.
7. Open a Chrome browser and type the URL <a href="http://localhost:3000/" >http://localhost:3000/</a><br/>
   This webpage will display a form to enter a number. Enter a number in the input field and
   click on the 'Submit' button. The fibonacci number(s) will be displayed in the webpage.

<b>Running the tests</b><br/>
The server needs to be running when performing these tests.
1. Can enter the following REST API query parameters in the browser URL and see the responses from the 	   server  
   a. <a href="http://localhost:3000/fibonacci?number=9" >http://localhost:3000/fibonacci?number=9</a></br>
   b. <a href="http://localhost:3000/fibonacci?number=-3">http://localhost:3000/fibonacci?number=-3</a><br/>  
   c. <a href="http://localhost:3000/fibonacci?number=0">http://localhost:3000/fibonacci?number=0</a><br/>
   d. <a href="http://localhost:3000/fibonacci?number=1468">http://localhost:3000/fibonacci?number=1468</a><br/>
   e. <a href="http://localhost:3000/fibonacci?number=1480">http://localhost:3000/fibonacci?number=1480</a><br/> 

2. From the command-line prompt can try the following curl commands with responses from server </br>
   a. $ curl -s http://localhost:3000/fibonacci?number=5 </br>
      [0,1,1,2,3]

   b. $ curl -s http://localhost:3000/fibonacci?number=-2 <br/>
      Negative number is not a valid number to generate Fibonacci number

   c. $ curl -s http://localhost:3000/fibonacci?number=0 <br/>
      Needs at least 1 to generate the first fibonacci Numbers

   d. $ curl -s http://localhost:3000/fibonacci?number=1477 <br/>
      Due to array size limitation the number needs to be between 0 and 1468

   e. $ curl http://localhost:3000/fibonacci?number=1477 <br/>
      % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
      100    70  100    70    0     0   4375      0 --:--:-- --:--:-- --:--:--  4375Due to array size limitation the number needs to be between 0 and 1468

   f. $curl -X POST -H 'Content-Type: application/json' http://localhost:3000/fibonacci

3. The Mocha test framework is used to test the HTTP GET and POST methods. The test file contains 
   8 test cases and it is located in RestApiWebService/test/app_test.js. <br/>
   From the Git Bash command-line prompt in the 'RestApiWebService' directory type the following <br/>
   $> npm test

4. <b>Project Directory Structure</b></br>
   RestApiWebService
    |--- node_modules  (javascript library files and modules)
    |--- out
    |    --- app.js.html   (JS Documentation for the app.js source code in html format)
    |    --- index.html    (JS Documentation for the project)
    |--- public
    |    --- css
    |        --- style.css (CSS code for views/index.ejs. Used in UI "http://localhost:3000/".
    |--- test
    |    --- app_test.js  (test code for app.js)
    |--- views
    |    --- index.js     (UI for "http://localhost:3000/")
    | --- app.js          (source code for the application)
    | --- jsdoc.json      (Contains information on dependent files for JSDoc and docdash template)
    | --- package.json    (Contains information on dependent files for node modules, scripts)  
    | --- README.md       (Readme file for steps to deploy and run this project).

    The documentation for this project is located in RestApiWebService/out/index.html and it can be opened in a Client Browser.

<b>Prerequisites</b> <br>
Node.js 8.11.2 from https://nodejs.org/en/download/ <br>
Git from https://git-scm.com/downloads <br>
Git bash for Windows from https://git-scm.com/download/win <br>

<b>Built With</b><br>
NodeJS 8.11.2 for server side javascript source code<br>
Express 4.16.3 for REST API service<br>
Mocha 5.2.0 test framework for unit testing<br>
chai 4.2.0 module for testing<br>
supertest 3.3.0  module for testing<br>
ejs 2.6.1 is JavaScript template to render HTML<br>
jsdoc3 to generate documentation for this project<br>
Sublime Text 3 to open project and view/edit source code

<b>Versioning </b><br>
SemVer versioning 1.0.0

<b>Project Limitations</b><br/>
1. Largest number that can be entered as input is 1468. After testing numbers greater than 1468 it was obvious that blank spaces and nulls were getting added to the array data structure.
2. The project requirement is to input a number and generating a sequence of fibonacci numbers. This requirement was implemented with the REST API GET and POST methods. Based on the scope of this project it was not necessary to use PUT and DELETE HTTP methods to meet the requirement

<b>Authors</b> <br>
Leena Rex 

<b>License</b> <br>
This project is for demo purpose only.
