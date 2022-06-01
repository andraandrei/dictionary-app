# dictionary-app

This application is a REST API that allows to know if a word exists and its meaning (English). It also allows to add words to a custom dictionary, as well as to delete these words. 

To make this application I have used Java Spring Boot.


## What was my motivation and what did i learn?

What motivated me to carry out this project was the desire to carry out a practical case by myself, from scratch and using my own resources and in this way put into practice the knowledge acquired in the course in a practical way in a real case. 

In this project I have learned the concepts of a REST API and HTTP communications, using Spring Boot as a framework on top of Java. 

It has also helped me to be very self-sufficient and to search for resources and find solutions autonomously in an unknown environment. 

## How to install and run the project



## How to use the project

Run the project and the REST API will bind to `http://localhost:8016`. The following endpoints have been defined:

- ### @GET /dictionary 

This endpoint requires the word variable to be passed as an argument to the request.

```
http://localhost:8016/dictionary?word=tree
```
It will first check if the word exists in the custom dictionary and return it if exists. If not, it will request to an external API (https://api.dictionaryapi.dev/api) the word defintion.

If the word does not exist, it will return an error message.

- ### @POST /setWord

This endpoint requires the body of the request to have an specific format

```
http://localhost:8016/setWord

{
    "word":"blablabla",
    "definitions":[
        "definition1",
        "definition2"
    ]
}
```
It will add the word and definition to the custom dictionary. 


- ### @DELETE /deleteWord

This endpoint requires the body of the request to have an specific format

```
http://localhost:8016/deleteWord

{
    "word":"blablabla",
    "definitions":[
        "definition1",
        "definition2"
    ]
}
```
It will delete the word, if exists, and definition in the custom dictionary. 