Questions
The following questions cover different areas of knowledge. You may not be able to answer them all. If there is a question that is clearly not relevant for the position you are applying for, we will not count it against you if you cannot answer it.
We expect each question to take one to two minutes on average.


Programming concepts

1. What is the difference between ++$a and $a++?
- $a++ returns value before incrementing
++$a increments a and returns incremented value

2. Can you explain the importance of late static binding? What is it, when would you
use it, why do we care?
- Late binding for all non-final, non-private instance methods.
This is how polymorphism is implemented

3. What is the difference between a closure, a callback, a lambda, and a promise?
- A Closure is an inner function that accesses to the outer function's variables.
A callback is a function that is passed to another function as a parameter
A lambda is an anonymous function, designed to be used once
A promise is a callback handle to do something asynchronously, and when work is done,
the promise's 'then' function is triggered.

4. Explain logic short-circuiting, and how it can affect the code you write.
- true || **** ; meaning if left side is true and right side after the OR is not evaluated
// true

5. What is eager loading, and what are the pros and cons?
- pros: All data is loaded upon page loading. Eager loading is essential for games, at least loading everything required for a level.
When you are playing you don’t want any frames dropped, this is the reason you usually need
to sit through a “loading level…” screen
cons: Even not needed data is also loaded.

What to use, when
6. What is your opinion about where and when you should use protected versus private in class member definition?
- protected - Only this class and any subclasses may access the method/property.
private - Only this class may access the method/property. It won't even be inherited, Use when
variables/methods are designed to be hidden and not shared

7. When would you use a trait (or mixin) instead of classical inheritance, and why?
- classical inheritance is only from one parent class only
trait (or mixin) - can have multiple traits

8. Can you give an example of when you would use two different sorting algorithms
on the same data set, and why?
- To evaluate Time complexity and CPU resource usage.

9. When is it good to use a bitmask/bitset? Describe the advantages and
disadvantages.
- Bitset saves space, but they are badly readable if you want to work productively with raw SQL output

10. When would you use a regular expression, a parser, and a simple string search?
Give examples.
- regex is used in autocompletion in list filter searches.
parser is used in JSON response filtering for specific user data
simple string search for simple logic searches in boolean logic conditions
Practicalities

11. When is it appropriate to write unit tests, and when would you mock?
- Always use TDD to write tests first to fail, then pass and refactor if necessary.
mock when testing against API not yet available or database queries for consistency.

12. Give an example of how you would use defensive programming techniques to
ensure robustness.
- Use val or CONST to maintain immutability to prevent code changes by malicious hacking.

13. How can you tell quickly and simply whether MySQL is available on a remote
server, and whether a local means of connecting to it exists?
- use mysql client, if you have it installed it's quite easy to access a remote host
mysql -hyour_ddbb_server_ip -uyour_user -pyour_password your_database_name
or
mysql -h your_ddbb_server_ip -u your_user -p  your_database_name

14. Do you think it is good or bad to commit “built” files? (E.g. the output of SCSS, etc.)
Explain why.
- Bad idea. Otherwise your git diffs are going to be a huge mess and it’ll
be hard to identify when and what changes entered in the codebase.

15. What do you think about leaving out the closing tag in a PHP file?
- It is optional, and in some cases omitting it is helpful when using include
or require, so unwanted whitespace will not occur at the end of files, it will
still be able to add headers to the response later.

Databases
16. When would you use fully-normalised form, and when would you use JSON columns?
17. What is the difference between strict and schemaless data,and when would you use each?
18. What are the pros and cons of tabular polymorphism, and when would you use it or advise not to use it?
19. When would you use a stored procedure and why?
20. What is your opinion about modelling relationships using foreign keys versus
letting an ORM handle them?
21. When is ORM bad?
Personal
22. What is your pet hate coding smell, and why?
23. What was the most useful feature that was added to the latest version of your
chosen language? Please include a snippet of code that shows how you've used it.

24. Have you watched Mr Robot? (The dev team want to know!)
- Not yet, but if more people talk about it, will check it.

25. Please describe yourself using JSON.
- {
	"name": "Zahara",
    "city": "London, UK",
    "food": ["Asian", "Italian", "Japanese"]
}


Coding test

This coding test is designed to show us your thought process and approach, as well as demonstrate your skills. How much effort you put into it is up to you, but typically we would expect two to three hours is reasonable. Some people choose to spend more - that’s fine, but not required. You are welcome to stop whenever you like.
We are not expecting you to spend an insane amount of time on this. We feel that, using the right technologies, it is possible to achieve what the test asks for, in the timescale indicated. If you cannot achieve everything exactly as you would ideally like, let us know.
Feel free to ask us questions if you need to.

Technologies

Use whatever languages, frameworks, etc. you feel are best, or are most comfortable with, along with third-party libraries. This could be something spangly-new and cutting-edge, or old-school and boring - it’s your call. Points will not be won or lost based on this choice, providing it is fit for purpose for the requirements.
The only technology requirement that we have is that it should be able to run on Linux - either a standard Linux VM, or using AWS systems. Beyond that, you are free to specify architecture and system dependencies as you see fit.
Please choose an appropriate CSS framework or implement something so that what we review is pleasant to look at and shows some thought as to layout and interactivity.

Requirements

Create an application which will allow at least two users to log in simultaneously and manage items in categories. The categories should be in a hierarchy of potentially infinite depth. The items only require a label.
The users should be able to perform standard CRUD, plus if one user makes a change, the other user(s) should see the change (if appropriate) without manually refreshing their web browser.
Your solution should follow best practice, and be robust and scalable. We expect to see the same techniques and approaches that you would use in a real project.
User journeys
Mark wants to keep track of his belongings. He logs in, and is presented with a list of categories, showing the different levels visually. He adds “Electronics”, and under that, “Televisions”. To this category he adds the items “49-inch LCD”, “40-inch plasma”, and “32-inch CRT”.
Sandy logs in and creates “Gaming consoles”, and under this, the items “PS4 Pro”, “XBox One X”, and “Nintendo Switch”.
Mark sees Sandy’s entries appear. He edits “Gaming consoles” to sit under “Electronics”. This change appears on Sandy’s screen as soon as he has done it.

Bonus points

The following areas are not required, but if you choose to include them we will count them as bonus points.
● Authorisation (user levels, permissions, ACLs, roles, etc.) in addition to authentication. For instance, allowing some users to edit, and some to view only.
● Appropriate and sensible tests.
● Any other dimensions on the data that might be useful, e.g. tagging.
● Responsive design techniques for different screen sizes, mobiles, etc.
● Any form of notifications - e.g. toast, element styling - to alert the user that
something on their screen has changed.

Deliverables

Supply your efforts in a zipped Git repository, i.e. complete with the .git folder so that we can review your commit history, along with full documentation to set it up and run it on a Linux system. We will follow the instructions to the letter. If particular system components or services are required, include notes about their setup and configuration where it deviates from the default, out-of-the-box state. Note the version numbers of any system software required, if appropriate.
Please include any notes that you would like us to read, along with answers to the following questions:
● How long did you spend on the coding test?
● Did you manage to cover everything that you wanted to?
● What would you add to your solution if you had more time?
● Would you choose different technologies if this were to become a reliable
enterprise system? Why? Or, why not?

Feedback

Don’t forget to tell us what you thought of this test. Did you enjoy it? Was it fair? How could we improve it?

Marking

Please be aware that we are marking you on everything we see. We will evaluate how carefully you have read this brief, and whether you have supplied what we have asked. We will assess the quality of your code, your thought process and approaches; your attention to detail and whether you take pride in your work.
Please consider this carefully, because we are looking for developers that can fit in with our team, follow our processes, and produce what they are asked to without constant correction. Ability is hugely important, as is experience, but you will need to fit into the day-to-day process of shipping code that works, and keeping projects running smoothly.
Thank you
Thank you for taking the time to sit this test, and for expressing an interest in working with us. We greatly appreciate it, and we will give you honest feedback on how you have done - good or bad.
Good luck!
