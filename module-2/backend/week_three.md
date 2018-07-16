## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  - rails new <model_name>

2. What do Models generally inherit from in rails?
  - ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
  - ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  - resources :horses, only: [:index]

5. What rake task is useful when looking at routes, and what information does it give you?
  - rails routes.  It shows all the routes of the resources.

6. What is an example of a route helper? When would you use them?
  - horses_path.  When you are redirecting the controller or setting a path for a link.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
   - path only returns the url relative to your domain. For instance, root_path returns / while root_url returns http://mydomain.com/ You should  use url for redirects and path for hyperlinks.

8. What are strong params and why are they necessary?
  - They are the attributes of the resource. They provide security when a user is filling in a form.  

9. What role does `form_for` play in helping us create our forms?
  - It is a helper method that allows the user to create a form in the view.

10. How does `form_for` know where to submit the user's input?
  - It looks at what action in the index it is the template for.

11. Create a form using a `form_for` helper to create a new `Horse`.

  form_for @horse do |f|

  <%= f.label :name %>
  <%= f.text_field :name %>

  <%= f.label :age %>
  <%= f.integer :age %>

  <% end %>

12. Why do we want to validate our models?
  - Because we need input to fulfill the columns of the table to make sure it's created successfully

13. What are the steps of the DNS lookup?
  - 1) the client
    2) Resolving server
    3) Root
    4) Top level domain
    5) 


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  ```ruby
  class Horse

    def move
      prance
    end

  end
  ```
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  


16. What is inheritance?
    When a class is able to use all the methods of a module

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
