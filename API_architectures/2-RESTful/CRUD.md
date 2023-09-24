# CRUD (Create Read Update Delete):-

1. CREATE :
    - URl : 'www.medium.com/blogs'
    - http method : POST
    - data sent in form of `body params` :
      {
      title: '',
      description: ''
      }
2. READ :

    - API to read all blogs :-
        - URL : 'www.medium.com/blogs'
        - http method : GET
    - API to read a specific blog :-
        - URL : /blogs/:id --> {eg : '/blogs/2', '/blogs/3214963'}.
        - http method : GET

3. UPDATE :

    - API to update a blog :-
        - URL : 'www.medium.com/blogs/:id'
        - http method : PUT/PATCH
        - `body params` : {
          title: '',
          description: ''
          }

4. DELETE :

    - API to delete a blog :-
        - URL : 'www.medium.com/blogs/:id'
        - http method : DELETE

**_ NOTE : The ':id' can also be `human readable friendly id's` like {/segment-tree, /javascript-data-types, etc.} _**

## Slugs/Slug-id (`human readable friendly id's`) :-

-   A slug or slug ID is a user-friendly and URL-safe version of a string that is used to identify a specific resource in a web application.
-   They should also be unique to avoid conflicts with other resources.
-   eg :- `https://example.com/blog/introduction-to-web-development`
-   It improves search engine optimization (SEO), and provide a better overall user experience.
