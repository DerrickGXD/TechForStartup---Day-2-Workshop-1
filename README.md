# TechForStartup---Day-2-Workshop-1 (Client Server System Design)

# Codes
Coding Question : [Click Here](https://codesandbox.io/s/tech-workshop-question-client-server-system-design-s1ui3?file=/src/index.js)
<br/>
Full Working Code : [Click Here](https://codesandbox.io/s/tech-workshop-client-server-system-design-ohf50?file=/src/index.js)

**DO NOT** edit the codes on these link. If you want to have a copy of the code to work on, please fork it. Please try to attempt the coding question before looking at the full working code.

# Scenario
iCUBE would like to create a website to allow participants to register for Tech For Startups. To keep track of the name of participants who sign up, we will be using a server. For simplicity in our workshop, we will only keep track of the name of last participant who sign up. When a user signs up, the server should update its variable **name** with the name used to sign up. To ensure the website still keeps track of the name in another page, iCUBE creates another page. When the user clicks **Next Page** and goes to another page, the website can still retrieve the name from server.

The back end server script is `index.js`. The front end website scripts are `main_page.html` and `next_page.html`. We will be using **REST API** to communicate between front end and back end. In simple terms, the front end can request a query to back end with an endpoint starting with "/" and the back end will send front end with what it requests. We will be using **XMLHTTPRequest** in front end to submit a query and **Express.js** in back end to receive a query.

# Tasks
1. Identify how `index.js` receives a query via endpoints. When a server starts, it will first receive a query with "/". Currently after receiving "/", the server sends a message *Welcome to Tech For Startups!!*. Instead of sending this message, you should display `main_page.html` to show the registration page.
2. The registration page has a form to fill in first name, last name and team name. Clicking the submit button will request a query to the back end with endpoint "/register". `main_page.html` already has the code to request a query to the endpoint, alongside with first name, last name and team name. What you need to do is process the query in `index.js`. You should save the variable **name** with full name (first name + last name), and sends a reply to the front end with a message *{Name} From {Team Name} Has Registered!*. If `main_page.html` successfully recieves , the `main_page.html` should replace *Anonymous Has Registered!* with the message.
3. In `next_page.html`, write the **XMLHTTPRequest** to request **name** from `main_page.html`. Use the endpoint "/name" to submit a query. Refer to `main_page.html` on how to write **XMLHTTPRequest**. You should also replace the text *Anonymous* with the name that you requested.
4. In `index.js`, implement the GET query for the endpoint "/name" and send the variable **name** back to front end.
5. Check whether the code is working. At `main_page.html`, register a participants. Click **Next Page** and you should see **Well Done Anonymous** is replaced with **Well Done {name}**.

# TechForStartup---Day-2-Workshop-2 (Model View Controller)
