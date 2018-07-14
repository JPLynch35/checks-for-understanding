## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?  
rails new projectname -T -d="postgresql" --skip-turbolins --skip-spring  

2. What do Models generally inherit from in rails?  
Models generally inherit from ApplicationRecord  

3. What do Controllers generally inherit from in a rails project?
Controllers generally inherit from ApplicationController  

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?  
resources :horses, only: [:show]  

5. What rake task is useful when looking at routes, and what information does it give you?  
rake routes  
This shows you a table of all the path prefixes, verbs, urls, and controllers responsible  

6. What is an example of a route helper? When would you use them?  
comapanies_path is an example of a route helper for a comapny index page.  You would use them in your links, redirects or testing for ease of use (and general readability).  

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?  
_path provides the URI path where as _url provides the full URL with protocol included.  


8. What are strong params and why are they necessary?  
Strong params make sure that you are only utilizing the information that you actually want when making or updating an object.  

9. What role does `form_for` play in helping us create our forms?  
form_for is a helper method that eases the code required to build a functional form.  It also has 'magic' behind it that understands where it is caleld from and what the submit button should do (edit/create).  

10. How does `form_for` know where to submit the user's input?  
The form_for knows where to submit the user's input by the instance variable(s) directly after 'form_for'  

11. Create a form using a `form_for` helper to create a new `Horse`.  
<%= form_for @horse do |f| %>  
  <%= f.label :name %>  
  <%= f.text_area :name %>  
  <%= f.label :color %>  
  <%= f.text_area :color %>  
  <%= f.submit %>  
<% end %>  

12. Why do we want to validate our models?  
We validate our models so that we don't accidentally make and save incomplete data.  

13. What are the steps of the DNS lookup?  
Browser talks to the OS  
If the address is not cached, the OS reaches out to the local DNS server.  
If not found, this reaches out to the Root server.  
If not found, this reaches out to the Top Level server.  
If not found, this reaches out to the Authoritative Name server.  

### Review Questions  
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?  
def move  
  prance  
end  

15. Given the following hash:  

```ruby  
furniture = {table: {height: 3, color: "red"}, purchased: true}  
```  
What is the different between how you would return true vs returning 3?  
3) furniture[:table][:height]  
true) furniture[:purchased]  

16. What is inheritance?  
Inheritance is gaining attributes and behaviors from the parents/grandparents/etc  

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week