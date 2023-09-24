# REST (Representational State Transfer) :-

-   REST is a convention.
-   `Every real life entity is expected to be represented as a resource`. REST heavily relies on the term resource.

    -   eg : `banglore/movies/drishyam-2` --> here 'banglore' | 'movies' | 'drishyam-2' they are all resource.
    -   when we hit 'banglore' --> we will see all shows/movies/events in banglore.
    -   when we hit 'movies' --> we will see all movies in banglore.
    -   when we hit 'drishyam-2' --> we hit a singular resource, which is the movie name we were looking for.

-   Everytime with a RESTful API request, we have to send the `type(methods like GET, POST, etc.)` of the request.
-   `VIMP` : `In rest conventions, data/messages sent apart from URL are sent in JSON format`.
-   eg :- Rest API for a blog;
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

-   We can use any method for any task(like GET to delete a resource, POST to get a resource, etc.), but usually we follow a specified convention like below.

1. GET : `retrieve info about a resource`.
2. POST : `submits an entity to the specified resource. change in state or create side effects on a resource`.
3. PUT : `make complete update on a resource`.
4. PATCH : `make partial update on a resource`.
5. DELETE : `delete a resouce`.

## HTTP methods supported by HTML5 :-

-   html5 forms supports only `GET and POST` requests.
-   Then how do we use other HTTP methods ?
    -   Using JS.
    -

## 3-Ways to send data :-

-   In general RESTful API conventions, the 3 ways to send data are :-

1. Request Params :

    - Request params are part of the URL path and are typically used to `identify a specific resource or entity in the URL path.`
    - Generally unique identifiers are passed in as request params.
    - eg :- `"/movies/blackpanther"`.

2. Query Params :

    - Query params are key-value pairs appended to the end of the URL after a question mark (?) and separated by ampersands (&).
    - Used for providing additional information or filtering criteria in the URL.
    - Generally used for preparing filteration criterias or pagination criteria.
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

## GET vs POST by REST convention :-

| GET                                                                                                               | POST                                                                                                                                                                                                  |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| In get request data is sent mostly in url, that means it gets saved in our history. we can log it, cache it, etc. | generally data is not expected to be sent in URL, rather than in `request_body/payload`.                                                                                                              |
|                                                                                                                   | since data is not saved on client side, it is bit more secure.                                                                                                                                        |
|                                                                                                                   | So we can use this for Authentication, generate_OTP(it looks like we are fetching the OTP but it first generates an OTP logs in in the server and then sends a response so it comes under POST), etc. |
|                                                                                                                   |
