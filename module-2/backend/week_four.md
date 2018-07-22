## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  -a cookie is a file or more specifically a hash that stores information about the specific client
2. What’s the difference between a session and a cookie?
  -cookie is stored on the client's machine whereas a session is stored on the server
3. What’s a flash and when do you want to use flashes?
  -A flash is a message that pops up on the screen usually when a form is submitted and the flash message is set up differently depending on if it was submitted successfully or unsuccessfuly.
4. Why do people say “HTTP is stateless”?
  -Because all requests are read the same way and don't have any stored attributes unless sessions and cookies are used.
5. What’s authentication? Explain.
  -It is defining who the user is. For example are they are visitor, registered user or an admin.
6. What’s the difference between authentication and authorization?
  authentication is defining who the user is ie a visitor, registered user, admin. etc.  Authorization is defining where and what you're allowed to do on a website.
7. What’s a before filter?
  -code that automatically runs before an action
8. How do we keep track of a user once they’ve logged in?
  -we assign the user id to a session id.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  -You would want to namespace a resource when you want to separate controllers.  You want to nest a resource when it is dependent on its parent such as comments.
10. At a high level, what tools can you use to implement authorization? How would you use them?
  -enums which is a organized way to delineate a user from an admin.  Namespacing which allows admins special access and abilities to create and delete resources. And before filters which allow you to see what type of user is trying to access the page before anything runs.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  -an enum acts as a pseudonym for a string  for example when using auth we can say role: user or role: admin but with namespacing we can use and array(or hash) and say role: 0 or role: 1 based on the indexes we set up our enum with.
12. What are some strategies you can use to keep your views DRY?
  -Don't make class method calls from them and try to have most of the logic in the model or controller.

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```
given.sort_by! { |hash| hash[:holiday][:name] }

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
given.gsub(/[$]/, '').to_i


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
