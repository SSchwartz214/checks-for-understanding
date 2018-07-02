## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET: Render a resource
  POST: Create a new resource
  PUT: Change all parts of a resource
  PATCH: update part of a resource
  DELETE: Delete a resource

2. What is Sinatra?
  It's a framework that allows us to interact with the web/internet with Ruby code.

3. What is MVC?
    A design protocol used for creating web apps.
    Model: data logic
    View: presentation logic
    Controller: app logic

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
    To make it easier for users to navigate the website and for developers to be able to read other devs code.

5. What types of variables are accessible in our view templates without explicitly passing them?
    instance variables

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
```ruby
  get '/horses' do
    locals: {name: 'Mr. Ed'}
  erb :index
end
```

8. What's the purpose of ERB?
  To merge HTML and ruby to make web apps.  You can then right Ruby code in HTML.

9. Why do I need a development AND test database?
  It would be very risky to make changes to the development db without knowing the app works correctly.
  Therefore, you create a test db so you can run your tests based on this database without risking
  making negative changes to the development db.

10. What is CRUD and why is it important?
  Create, Read, Update, Destroy.  It is important when working with databases as
  it allows the app to modify the database correctly and efficiently.

11. What does HTTP stand for?
  Hypertext transfer protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <%= %>: executes and displays code
  <% %>: executes and does not display code

13. What's an ORM? What does it do?
  Object relational mapper.  It acts as the middle man between the database and Ruby objects.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

16. What's a migration?
  A set of rules to edit/update our database

17. When you create a migration, does it automatically modify your database?
  no, you then have to run rake db:create and rake db:seed to modify the db

18. How does a model relate to a database?
  A model creates and holds the class and all methods of that class that the db data is representing.

19. What is the difference between `#new` and `#create`?
  Create makes and saves the data in the table whereas new just makes it but does not save it anywhere.


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?

```ruby  
def create_seeds(file_path, model)
  opened = CSV.open(file_path, headers: true, header_converters: :symbol)
  opened.inject(0) do |row|
    row_hash = row.to_h
    model.create!(row_hash)
  end
end
```

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
  activities[:hiking][:supplies].push("granola bar")

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  DRY: Do not repeat yourself

### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
