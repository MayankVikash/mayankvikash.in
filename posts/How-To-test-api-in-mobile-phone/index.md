---
title: How to test API on your mobile phone
description: Detailed guide to test an API with API Tester mobile app.

cover: https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/How-To-test-api-in-mobile-phone.png

---
![How to test API in mobile phone](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/How-To-test-api-in-mobile-phone.png)

Testing APIs is really hard and complicated. Today I am going to show how to test an API and that too on your mobile phone. I will show an easy approach. Let's start by learning What is API?

API is abbreviated for Application Program Interface. It is a way for two or more computer programs to communicate with each other. Let's learn this with an easy example. In India, IRCTC (Indian Railway Catering and Tourism Corporation) manages all the Railway's services. It manages the booking of tickets, food and all other things. You can book your ticket either online or offline through the reservation counter. If you are booking it online, you would likely book it directly from the IRCTC website or app or through private ticket booking services like IXIGO.

When these private companies book a particular seat or IRCTC itself books one. It needs to inform other services that this particular seat has been reserved and not sell this seat again to another passenger. To communicate with each other, these services use API.

The same is the case with the booking of flight tickets.

### All about GET, POST, PUT and DELETE request methods

HTTP requests are at the heart of every web application API. These are the messages your browser sends to the webserver to get the resources it needs. This can be anything from a webpage to an image to a JavaScript file.

Testing HTTP requests ensures that your web application works as intended. This allows you to troubleshoot issues and verify that your application is working correctly.

How do HTTP requests work?

The Hypertext Transfer Protocol (HTTP) was created to make it possible for clients and servers to communicate.

A client sends an HTTP request to a specified host that is on a server, so the request is made to access a server resource.

The client uses a URL (Uniform Resource Locator) that contains the data required to access the resource to submit the request. The parts of a URL clarify what a URL is.

The following components are present in a properly constructed HTTP request: − An inquiry line.

− A set of header fields or HTTP headers.

− A message body.

### GET and POST are the two most used HTTP methods.

#### Why is API request Tested?

To ensure that your API responds appropriately to a wide range of expected and unexpected queries, it is crucial to test it. This procedure is intended to verify the API's dependability, performance, and security in addition to its functionality.

API testing is particularly significant since it offers various advantages over other forms of testing, such as unit and UI testing.

#### Tools for testing API?

Testing HTTPS requests can be complex because many different tools are available, and it can take a lot of work to know which one to use. Here are some of the best tools for testing HTTPS requests:

1. Charles Proxy - This powerful HTTP/reverse proxy tool can test HTTPS requests. It has a built-in SSL decryption feature that makes it easy to view and analyze HTTPS traffic.

2. Fiddler - This is another popular HTTP debugging tool that can be used to test HTTPS requests. It also has a built-in SSL decryption feature that makes it easy to view and analyze HTTPS traffic.

3. Wireshark - This network protocol analyzer can capture and analyze traffic, including HTTPS traffic. It can be helpful for troubleshooting and debugging purposes.

4. curl - This is a command-line tool that can make HTTP/HTTPS requests. It's a valuable tool for testing and debugging purposes.

5. Postman - This is a popular graphical user interface (GUI) tool that can be used for making HTTP/HTTPS requests and viewing responses. It's very user-friendly and easy to use, making it a good option for those unfamiliar with command-line tools like curl.

These tools require expertise in a programming language and are used on PCs. Sometimes, for beginners, they are challenging to use.

### How to test HTTP requests from a mobile phone?

The previous paragraph listed desktop API testing tools, but in today's fast-paced world, more and more people work directly from smartphones using API testing mobile applications. They provide a simple, mobile-friendly experience for your continuous work. You are not required to take your laptop on the road. It is a more productive way to test beginners and experts for speed and productivity.

In this article, I will show you how to test various HTTP requests with clear examples using API Tester mobile application.

API Tester is a completely free tool available for [Android](https://play.google.com/store/apps/details?id=apitester.org) and [iOS](https://apps.apple.com/us/app/api-tester-debug-requests/id1575521212) that may be downloaded from AppStore or Google Play.

You can run any test using its powerful editor and API testing environment. It supports any type of API: REST, GraphQL, WebSocket, SOAP, JSON RPC, XML, HTTP, HTTPS, and allows you to make all types of HTTP requests: GET, POST, PUT, PATCH, DELETE, HEAD, OPTIONS, COPY, LINK, UNLINK, PURGE, LOCK, UNLOCK, PROPFIND, VIEW.

Now let's try to test some of the most popular methods GET, POST, PUT and DELETE using API Tester mobile app.

### GET Request Method

The GET method is an HTTP technique used when requesting data from a specific origin. It can also be used to extract a particular component from a group.

### Testing GET Method

Once you download and open API Tester mobile app, you can see the “Create new request” button. When you click on it, the next step is to select the request type. We will take these actions for each new request.

![https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/1.PNG](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/1.PNG)

So, I click on the GET option, and the next screen shows the untitled request (you can rename it for your convenience).

To perform the request, we need to provide the API URL and paste it into the section starting with HTTPS://.

You can see multiple options for the requests, like adding headers, cookies and query parameters. Also, you can add Authorization details with the Basic and OAuth options.

I have the grocery store API [https://simple-grocery-store-api.glitch.me/products](https://simple-grocery-store-api.glitch.me/products), and it is available publicly. So, I’ll put it in the URL section and click on the “Play” button in the top right corner.

![https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/2.png](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/2.png)

Here is the response we got, where you can see the product list and then examine it according to requirements: it shows the category, name and availability.

![Image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/3.png)

You can inspect this response and see that 200 is a success. It took 6.39 milliseconds, and the response was 1.7 KB.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/4.png)

### POST Request Method

The HTTP method known as POST allows users to submit large amounts of data from a defined source to a server. Most HTML forms on the Internet use this request technique. This technique can supply data as a package in a separate conversation with the processing script. As no parameters are transmitted along with the URI, data sent via the POST method cannot be seen in the URL.

POST requests can be used to upload files or submit online forms. However, ensuring that the format is compatible with the receiving program is vital. An HTTP POST should be formatted with HTTP headers, a blank line, and then the request body. The Information header indicates the POST request's body type.

POST, the HTTP request's message body contains form data that may be seen. While the POST method's answer can be stored, it is not idempotent. POST request parameters are more secure since they cannot be cached, cannot be kept in the browser's history, do not have a limit on the length of form input, and cannot be bookmarked.

### How to Test POST Method

Let me show you an example of how to create a POST method. We will post data to the server with a request using the API Tester App. This data is about user signup using the URL [https://petstore.swagger.io/v2/user](https://petstore.swagger.io/v2/user), and I will send user information details, including username, first name, last name, email, password, and phone number, in a request to the server.

First, open the app and create a new request. Select the POST method, and a new screen shows the untitled request. Here you can add different options: specify data in these tabs, like adding cookies, Authentication required by your server, and queries.

In the body section, you can see an option called “Raw”, which contains “Content-type” and “Post Data”. What does it mean?

**Content type** means the format of the data type you want to send to your server, and **Post Data** is an option in which you can write your data format.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/5.png)

In the Content type, you can utilize different options by default: Application**/JSON** format, which we will use. But if your API supports **XML** or plain text, they can also be utilized.

In this example, I am using a simple API, and I have details of the user that I want to post to the server in **JSON** format.

So, in the Post Data, I wrote my data, which was automatically saved.

.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/6.png)

After clicking the “Play” button, you can see I got a response successfully with a 200 status code in 2.59s. My data has been successfully posted to the server.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/7.png)

### PUT Request Method

The HTTP PUT request method replaces a representation of the target resource with the request payload or creates a new resource.

PUT and POST are different because PUT is idempotent, meaning that calling it once or many times in a row has the same impact (with no side effects). In contrast, several identical POST requests may have different results, like placing an order many times.

The origin server makes a 201 (Created) response to the user agent if the target resource does not currently have a representation and the PUT request successfully creates one.

The origin server must deliver either a 200 (OK) or a 204 (No Content) response to indicate successful completion of the request if the target resource does contain a current representation and that representation is successfully changed in line with the state of the enclosed representation.

This is how a PUT request works and lets more discover it using API Tester mobile app.

### Generating PUT Request

For creating the PUT request, I have used the Open Source API, whose URL is [www.reqres.in](http://www.reqres.in). In the previous chapter, I posted data on the server through the Post method, and now, with the PUT Method, I want to update the Job role.

Create a new PUT request and add the information you want to update, as we did in the POST method. In the Post Data section, I’ll paste the user’s name and job role in **JSON** format.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/8.png)

Now, after pasting the information and clicking the “Play” button, you can see the successful response with a 200 status code. In 1.34s, my data is successfully updated in the API and sent to the server using API Tester mobile app.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/9.png)

### Delete Request Method

The resources are deleted via the DELETE APIs, as the name implies (identified by the Request-URI).

The DELETE command is irreversible. A resource is deleted from the collection of resources when you DELETE it.

According to some, it renders the DELETE method non-idempotent. It is a topic for debate and individual opinion.

Those items should be regarded as stale if the request goes through a cache and the Request URI specifies one or more presently cached entities. This approach does not allow caching of results.

If the answer contains an object defining the status, a successful response to a DELETE request should be an HTTP response code 200 (OK).

202 (Accepted) is the correct status if the action has been queued. If the action has been completed but no entity exists in the response, the status should be 204 (No Content).

Repeatedly using the DELETE API on that property won't change the results. However, doing so a second time will result in a 404 (not found) response because the resource has already been deleted.

### How to Test Delete Method

The delete method is used to remove information from the server through the API. Using the Delete method is very easy through the API Tester app.

Open the App, create a new request, and choose the Delete method in the list mentioned. Enter the API base URL that you want to remove data from the server.

I want to delete previous information I posted to the server [https://petstore.swagger.io/v2/user](https://petstore.swagger.io/v2/user) in testing the POST request by adding a forward slash followed by my username “tester01” at the end of the URL. My information as a user is stored on that server.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/10.png)

Then click the play button to see response code 200 on the screen, which confirms that my user information has been successfully deleted from the server.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/11.png)

It can be deleted once; after trying, you can get a 404 error, meaning no information is left on the server.

![image](https://mayankvikash.in/posts/How-To-test-api-in-mobile-phone/12.png)

## Conclusion

In this article, we have analyzed what HTTP requests are, and what the most popular methods GET, POST, PUT and DELETE are used for. We have determined why it is important to test the API and what tools are used to perform it.

We also tested the above request methods using public APIs and the API Tester mobile application with illustrative examples.

- Written by Mayank Vikash
- Published on 19th December 2022 Monday 21:27 IST
- Last updated Dec 21, 2022, Monday 23:50 IST
