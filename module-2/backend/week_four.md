## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?  
A cookie is an identifier for a site visitor that lives on the visitors machine.  
2. What’s the difference between a session and a cookie?  
A session is stored server-side, a cookie is stored client-side.  
3. What’s a flash and when do you want to use flashes?  
A flash is a pop up message to let the user know of an action.  It can be used when an account is successfuly created, or when they enter incorrect credentials while logging on.  
4. Why do people say “HTTP is stateless”?  
HTTP is stateless because no information persists between requests.
5. What’s authentication? Explain.  
Authentication is verifying a login and password with the stored information in a database.  
6. What’s the difference between authentication and authorization?  
Authentication is logging in as a verified user.  Authorization is the differentiation between levels of access once logged in (user vs admin).  
7. What’s a before filter?  
A before filter ensures an action is completed prior to other actions.  
8. How do we keep track of a user once they’ve logged in?  
We track logged in users via sessions, specifically we have been using session[:user_id], which has a value of the user id.  
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?  
Namespace- when you just want to add a prefix to specific routes (admin/items/:id).  
Nest- this places one resource into another (artists/:id/songs), it is a method of organization.  
10. At a high level, what tools can you use to implement authorization? How would you use them?  
Authorization tools include adding roles to users, along with enums.  Roles will identify the user access level while the enum will identify their level of access with titles (aka: default, admin, etc).  
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?  
An enum is a way to identify a numeric flag in an object but be able to call upon it with a method that makes sense.  An exmaple is 0 bein a default user while 1 is an admin.  You decalre an enum in the model.  
12. What are some strategies you can use to keep your views DRY?
To keep your viewss DRY, you can utlize partials.  These will print the same things over and over across multiple views, but only have to be typed once.  You can also create helper methods in the application controller that will allow you to repeat methods across the models/controllers.  


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
[[0][:holiday][:name], [1][:holiday][:name], [2][:holiday][:name]].sort!

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?  
string.remove('$').to_i


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
