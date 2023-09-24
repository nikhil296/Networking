# REST (Representational State Transfer) :-
- REST is a convention.
- Every real life entity is expected to be represented as a `resource`. REST heavily relies on the term `resource`.
- Everytime with a RESTful API request we have to send the `type(methods like GET, POST, etc.)` of the request.
- In rest conventions, data/messages sent apart from URL are sent in JSON format.
- eg :-  Rest API for a blog;
    ```js
    // Task   : CREATE
    // method : POST
    // URL    : /blogs
    data sent in form of `request body`
    {
        name : '';
        description : '';
        created : '';
    }
    ```

## HTTP request methods and it meaning in REST conventions :-
1. GET      : `retrieve info about a resource`.
2. POST     : `create side effects on a resource`.
3. PUT      : `make complete update on a resource`.
4. PATCH    : `make partial update on a resource`.
5. DELETE   : `delete a resouce`.

## 3-Ways to send data :-
- In general RESTful API conventions the 3 ways to send data are :-
1. Request Params :
    - Request params are part of the URL path and are typically used to `identify a specific resource or entity in the URL path.`
    - eg :- `"/movies/blackpanther"`.

2. Query Params :
    - Query params are key-value pairs appended to the end of the URL after a question mark (?) and separated by ampersands (&).
    - Used for providing additional information or filtering criteria in the URL.
    - eg :- `"/categories/electronics?company=samsung&order=desc&filter=price"`

3. Request body :
    - Request body contains the data sent in the body of an HTTP request. 
    - It is commonly used in POST, PUT, and PATCH requests to send data to the server for creating or updating resources. 
    - The payload can be in various formats such as JSON, XML, or form data. Here's an example:
        - ```js
            POST /users
            Content-Type: application/json

            {
                "name": "John Doe",
                "email": "john@example.com",
                "age": 25
            }
         ```

## GET  vs  POST by REST convention :-
- GET :
    - In get request data is send mostly in url, that means it gets saved in our history. we can log it, cache it, etc.

- POST :
    - generally data is not expected to be sent in URL, rather than in `request_body/payload`.
    - since data is not saved on client side, it is bit more secure.
    - So we can use this for Authentication, generate_OTP(it looks like we are fetching the OTP but it first generates an OTP logs in in the server and then sends a response so it comes under POST), etc.