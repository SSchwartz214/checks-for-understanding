### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  -flash[:notice] = "message"

2. Where is cart information/temporary information usually stored?
  -In the session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  -Because it can change a lot which would require a lot of db calls and user would have to be logged in for things to save so a visitor could not add things to the cart.

4. What is the purpose of the asset pipeline?
  To compress files to make them register in the browser more quickly.

5. Why do we precompile our assets?
  So the browser understands the language we are writing in

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
  1) links css files
  2) links a javascript file
  3) puts an image on a page

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  - A description of the app, instructions on how to use the app, include an image.

8. What are the top four accessibility issues that we as developers should be aware of?
  -different browsers, different operation systems.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  -Callback. We would use in in a model we are making a slug for.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
scope :users, where(active: true)


11. What is the difference between a scope and a class method?
  The syntax.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
    -cart["48"] = 4

  12b. How would you increase the quantity of item 29?
  cart["29"] += 1

  12c. How would you find out how many items your user is thinking about purchasing?   


13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  -when a model can belong to more than one other model, on a single association. This means a subclass can override a method of the base class.  Ducktyping is when code will accept any object that has a particular method.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?
given.gsub(/" "()-/,".") 


### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel overwhelmed by the content presented this week
