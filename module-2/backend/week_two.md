## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?  
ActiveRecord is a DSL that ties Ruby and SQL together, with an easier to write language than SQL.  It allows you to code faster and more efficienty, although at the cost of full functionality of all SQL commands for advanced queries.  

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?  
Team.all  
Team.find(1)  
Team.order(:attribute)  
You have access through these methods through ActiveRecord.  The methods are inherited because of "< ActiveRecord::Base".  

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?  
Team.find(4)  
Owner.find(Team.find(4).owner_id)  

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?  
Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.  
one(teacher)-to-many(students)  

6. Define foreign key, primary key, and schema.  
Primary key- the id of the table, this is a unique number for the objects (rows)  
Foreign key- When a primary key (id) of another model (table) is applied as a column  
Schema- A file that shows the column blueprint of your tables in your database (as they currently are)  
7. Describe the relationship between a foreign key on one table and a primary key on another table.  
A foreign key on one table IS the primary key on another table  
8. What are the parts of an HTTP response?  
Status line (with a status code and reason phrase)  
Headers  
Body (optional)  

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.  

2. Name your three favorite ActiveRecord rake tasks and describe what they do.  

3. What two columns does `t.timestamps null: false` create in our database?  
created_at  
updated_at  

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?  
one-to-many  

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?  
the foreign key, teacher_id, within the school table  

6. Give an example of when you might want to store information besides ids on a join table.  

7. Describe and diagram the relationship between patients and doctors.  
many-to-many  

8. Describe and diagram the relationship between museums and original_paintings.  
one-to-many  

9. What could you see in your code that would make you think you might want to create a partial?  
repeating patterns (headers, footers, etc)  

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources  
**Exception being the HTTP response question  

Choose One:
* I feel comfortable with the content presented this week  
