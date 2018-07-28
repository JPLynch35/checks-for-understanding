### Week 5 Questions
1. How do we make flash messages display on a page?  
A flash message is usually nested in some logic within the controller. The format is flash[:success] = "Successfully did a thing!", this is an example of a success message. In order to display it on any page, you place the flash message display function inside your application.html.erb file as such:  
<% flash.each do |type, message| %>  
<%= content_tag : div, message.html_safe, class: type %>  
<% end %>  

2. Where is cart information/temporary information usually stored?  
In the session.  

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?  
Storing cart information in a database decreases performance as it has to do a lookup each time across the entire database.  Storing it in the session is much faster to retrieve.  If you wanted your logged in users to keep items in their cart between logins, then you would then need to use a database solution.  

4. What is the purpose of the asset pipeline?  
The asset pipeline minimizes our app, for faster performance in production mode.  

5. Why do we precompile our assets?  
We precompile our assets in order to minimize their size, for faster read times by computers.  

6. What do each of the following tags do?  

```ruby 
<%= stylesheet_link_tag "application" %>  Links a stylesheet to an html.erb file
<%= javascript_include_tag "application" %>  Links a javascript file to an html.erb file  
<%= image_tag "rails.png" %>  Adds an image to an html.erb file  
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?  
Some elements of a great readme are clear instructions on how to use the app, clear examples of using the app, and instructions on how developers can load up the app to make changes.  The benefits of a good readme are that more developers/users will be more willing to use your app, which is the entire purpose in making it to begin with.  

8. What are the top four accessibility issues that we as developers should be aware of?  
-site navigation  
-site structure  
-text  
-images  
It is important to make all these easier to use/see and to not introduce bias into your web app.  

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?  
This is an example of a callback.  Usually, you would find a before_save in your app if you utilize a slug in a URI somewhere (the before_save would save a parameterized version of the name/title as the slug).  

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```
scope :active, -> {where(active: true)}

11. What is the difference between a scope and a class method?  
From what I have read, there isn't much difference between a scope and a class method.  Scopes seem to just be cleaner/shorter (or syntax sugar) compared to regular class methods.  



### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  cart['48'] => 4  
  12b. How would you increase the quantity of item 29?  
  cart['29'] += 1  
  12c. How would you find out how many items your user is thinking about purchasing?   
  cart.values.sum  
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
Polymorphism is utilizing a common ground between associations that are very similar. Duck-typing is the idea that you can call actions on objects, and they may be performed if they are of similar type, looking at will it happen rather than can it happen.  We use these in Rails with our db connections.   

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
string.parameterize.replace('-', '.')


### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources 

Choose One:
* I feel overwhelmed by the content presented this week
