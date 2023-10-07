Paste the below URL in POSTMAN with the API method given below 

Register User : 

POST - 
http://127.0.0.1:8000/blog/register/
Give this by selecting RAW--> JSON type.

eg:
{
        "first_name": "TestUser",
        "last_name":" Test",
        "username": "test123@gmail.com",
        "password": "test123" 
},

Login User : 
POST- 
http://127.0.0.1:8000/blog/login/
Give this by selecting RAW--> JSON type.

{
        "username": "test123@gmail.com",
        "password": "test123" 
}

CRUD Operation for Blogs by authenticated user :

POST-
http://127.0.0.1:8000/blog/blogpost/
Give this by selecting form-data and adding title, content, and main_image in the KEY Field and giving the details in the value field 

To fetch all created blogs:

GET- http://127.0.0.1:8000/blog/blogpost/

To update specific fields of specific UUID
PATCH - http://127.0.0.1:8000/blog/blogpost/
Give this by selecting RAW--> JSON type.


{
    "uid": "a4b72563-ac02-40d9-b171-4a63cd8d05c4",
    "title": "This is used for testing the PATCH method"
}

To delete specific blogPost
DELETE - http://127.0.0.1:8000/blog/blogpost/
Give this by selecting RAW--> JSON type.

{
    "uid": "a4b72563-ac02-40d9-b171-4a63cd8d05c4",
}



To Logout the Loggedin User:

http://127.0.0.1:8000/blog/logout/
Give this by selecting RAW--> JSON type.

{
        "username": "test123@gmail.com",
        "password": "test123" 
}

To View the Blogs for Unauthorized Users: 
GET- 
 http://127.0.0.1:8000/blog/publicblog
