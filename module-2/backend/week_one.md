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
Sinatra is a domain specific language (DSL) used to quickly create web applications in Ruby. 

3. What is MVC?
MVC is an architectural pattern used to create web applications by separating the design into 3 distinct groups: Model, View and Controller. 

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
We follow conventions when creating actions/path names in order to create readable code and to pass state with a stateless protocol. 

5. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables

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


10. What is CRUD and why is it important?
C- create 
R- read 
U- update 
D- delete 
CRUD is the basis for web applications, standardizing the needed actions to change a database of any kind. 

11. What does HTTP stand for? 
Hypertext Transfer Protocol 

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= > This will display the Ruby output to the user
<% > This will not display the Ruby output to the user 

13. What's an ORM? What does it do?
Object Relational Mapping and wraps databases in object language, translating each row into an instance of a class. 

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
ActiveRecord 

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

16. What's a migration? 
A migration is the code that will create the schema for a table in a database, allowing it to be moved aroudn as needed from environment to environment. 

17. When you create a migration, does it automatically modify your database?

18. How does a model relate to a database? 
A model is the class of who's instances of that class create the rows in the database. 

19. What is the difference between `#new` and `#create`?


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

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

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.


### Self Assessment:
Choose One: (erase the others)
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources 

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
