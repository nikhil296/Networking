# Cookies :-
- ***`Why do we need cookies ?`***
    - Http is a stateless protocol, means the server does not store any info about the client.
    - but a lot of times server needs to maintain user session so what they do is they these information through Cookies mechanism on the client's system.
    - every time the client when sends a subsequent request to the server, this Cookie string is sent along with the http request header that helps the server in identifying, maintaing and serving content accordingly.
- ***`What is a Cookie ?`***
    - Cookies are small text files that are stored on a user's computer by a website they visit. 
    - They are commonly used by websites to store information about the user's preferences, login status, and browsing behavior.
    - Cookies are Unique Idetifier Strings that are `set by the server through http header`.
    - These mainly concerned towards privacy.
- ***`Set-Cookie header :`***
    - when a server wants to set a cookie it includes ***`js "set-cookie : value"`*** in the http response.
    - This value is stored in the cookie file of the browser.
- ***`How are cookies used ?`***
    - Cookies serve several purposes, including:
    1. `Session Management` : Cookies can be used to maintain information about a user's session on a website. For example, they can keep the user logged in as they navigate different pages.

    2. `Personalization` : Cookies can store user preferences and settings, allowing websites to customize the user experience based on their previous interactions.

    3. `Tracking and Analytics` : Cookies can be used to track user behavior, such as the pages they visit, the links they click, and the time spent on each page. This data can be used for website analytics and targeted advertising.

    4. `Advertising` : Cookies are often used for targeted advertising purposes. They can track a user's interests and display relevant ads based on their browsing history.