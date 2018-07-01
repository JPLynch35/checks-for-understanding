## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb. 
GET- renders a page  
POST- creates a resource  
PUT- updates an entire resource  
PATCH- updates part of a resource  
DELETE- deletes a resource  
  
2. What is Sinatra?  
Sinatra is a domain specific language (DSL) used to quickly create web applications in Ruby. It is a framework for web applications.  

3. What is MVC?  
MVC is an architectural pattern used to create web applications by separating the design into 3 distinct groups: Model, View and Controller.  

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?  
We follow conventions when creating actions/path names in order to create readable code and to pass state with a stateless protocol.  

5. What types of variables are accessible in our view templates without explicitly passing them?  
Instance variables.  

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?  
See below  
  
  ```ruby
  get '/horses' do
    @count = 1
    @name = 'Mr. Ed'
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?  
See above  

8. What's the purpose of ERB?  
So we can utilize Ruby syntax within HTML.  

9. Why do I need a development AND test database?  
The test database is cleared before and after every test is ran.  This is needed as different information is loaded and required for different tests.  The development database is equivalent to the production database, but is used in a development envrionment where mistakes can be made and not affect buisness.  

10. What is CRUD and why is it important?  
C- create  
R- read  
U- update  
D- delete  
CRUD is the basis for web applications, standardizing the needed actions to change a database of any kind.  

11. What does HTTP stand for?  
Hypertext Transfer Protocol  

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?  
<%= > This will display the Ruby output to the user.  
<% > This will not display the Ruby output to the user.  

13. What's an ORM? What does it do?  
Object Relational Mapping and wraps databases in object language, translating each row into an instance of a class.  

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?  
ActiveRecord  

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.  
1- GET /restaurants  
This takes a visitor to the restaurant index page.  
2- GET /restaurants/:id  
This takes the visitor to a show page for a specific restaurant with specific id.  
3- GET /restaurants/:id/edit  
This takes the visitor to a restaurant edit page with specific id to edit restaurant attributes.  
4- PUT /restaurants/:id  
This takes the edited attributes of a restaurant and changes those specific attributes in the database.  
5- GET /restaurants/new  
This takes the visitor to an add a restaurant page.  
6- POST /restaurants/:id  
This adds the new restaurant to the database.  
7- DELETE /restaurant/:id  
This deletes a restaurant from the database.  

16. What's a migration? 
A migration is the code that will create the schema for a table in a database, allowing it to be moved aroudn as needed from environment to environment.  

17. When you create a migration, does it automatically modify your database?  
No, after you create a migration (column parameters and all) you need to then call .migrate on the database to change it.  

18. How does a model relate to a database?  
A model is the class of who's instances of that class create the rows in the database.  

19. What is the difference between `#new` and `#create`?  
#new instantiates an instance of a class but does not save it to the database. #create instantiates an instance of a class and does save it to the database.  


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
-terminal: rake db:create  
-terminal: rake db:create_migration NAME=create_films  
-This will create your migration file that needs to be filled out with the object attributes (columns).  
-terminal: rake db:migrate  
-In the seeds.rb file you will need to write the code to read through (CSV.foreach) and create an object with each of the headers (true) in your CSV file.  
-terminal: rake db:seed  

21. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?  
activities[:hiking][:supplies] << 'granola bar'  

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.  
Encapsulation- restricting the access of data to only what needs it  
Abstraction- creating a digital representation of a real world item (a class instance)  
Inheritance- children inherit from their parents, grandparents, supersclass, etc.  
Polymorphism-  a method can share the name of another method, but will produce different results based on the type/class it is being enacted on  


### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
