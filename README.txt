Technology Stack:

Spring boot 2.6.7
Spring data repository
Mockito Junit
Java 8
Maven


Notes:

1. I have migrated the application to use spring boot features,
2. I created a restful Api that provides endpoints for returning list of cakes in json format and adding a new cake:

Running the Cake-Manager Springboot application
-----------------------------------------------

Since this is implemented using maven, please run mvn clean install -U.

you can either run com.waracle.CakeManagerApplication as a Java Application or mvn spring-boot:run 


1) For getting list of cakes in json please use the following urls:

http://localhost:9090/cakes  
http://localhost:9090/

2) To find a cake of a particular name use the following url:

http://localhost:9090/cakes/<name>

3) - For adding a new cake please use the following url:

url : http://localhost:9090/cakes
method: POST
json sample request format
{ 
 "name" : "cheese cake",
  "description" : "This is cheese cake",
  "image" : "http:imageurl/image"
}  

The above endpoint creates a new cake entry and on successful creation returns the status code 200 along with the list of all the cakes
including the newly created cake.

Things assumed not to be required for this test:
- logger implementation
- Sending a customized status code in response if a user tries to add a cake with the title already present. currently, it returns 500.
