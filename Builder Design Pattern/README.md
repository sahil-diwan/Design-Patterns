# Builder Design Pattern

Builder pattern is to avoid having complex constructors. In general, you should avoid having a constructor that takes a large number of parameters.
Because the below problems are faced
  1. Suppose we dont want to pass all the parameters to the constructor.
  2. If we want to pass all the elements we should know the sequence of the constructor also.
 
 A constructor with so many parameters is considered as a bad coding practice.
 Builder Design Pattern can help us in these situation
  1. It will make it easy to use such constructor.
  2. It will help us avoid writing such constructor.
  
  What problems builder design pattern solves ?
  
  Objects that need other objects or "parts" to construct them.
  
  <img src="images/test.PNG">
  <img src="images/1.PNG">
  
  First Create an address object , and multiple role objects and a collection to hold these role and then we can call our constructor.
  There are certain steps need to be followed to create user object.


# What is builder actually ?
  We have a complex process to construct an object involving multiple steps , then builder pattern can help us.
  In builder pattern we remove the logic related to object construction from "client" code and abstract it in separate class.
