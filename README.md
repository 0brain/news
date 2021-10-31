## **How to run app in a docker engine**

1) Clone current repository into your local directory 
```
git clone https://github.com/0brain/news.git
```
2) Change the default directory to working directory of a project
```
cd news
```
3) Run the application stack 
```
docker-compose up
```
4) Endpoint to use 
```
http://127.0.0.1:8000/articles/
```



## **API description**

- *related to articles*

Allows to display list of articles:
`GET: {{base.url}}/articles/` 

Allows to add a new article:
`POST: {{base.url}}/articles/`


Allows to display an article:
`GET: {{base.url}}/articles/{{article_pk}}/`

Allows to edit an article:
`PUT: {{base.url}}/articles/{{article_pk}}/`

Allows to delete an article with comments related to it:
`DELETE: {{base.url}}/articles/{{article_pk}}/`

Allows to implement button to upvote an article:
`PATCH: {{base.url}}/articles/{{article_pk}}/vote/`


- *related to comments*

Allows to display a list of comments related to certain article:
`GET: {{base.url}}/articles/{{article_pk}}/comments/`

Allows to add a comment to certain article:
`POST: {{base.url}}/articles/{{article_pk}}/comments/`

Allows to display a single comment of certain article:
`GET: {{base.url}}/articles/{{article_pk}}/comments/{{comment_pk}}/`

Allows to edit a single comment of certain article:
`PUT: {{base.url}}/articles/{{article_pk}}/comments/{{comment_pk}}/`

Allows to delete a single comment of certain article:
`DELETE: {{base.url}}/articles/{{article_pk}}/comments/{{comment_pk}}/`

## Postman collection link

https://www.getpostman.com/collections/2d7c26ea2fc2421e055e
