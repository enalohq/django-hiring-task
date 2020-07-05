#Assignment
This is a sample exercise which is similar to the kind of work you would be doing as an Intern at [Enable Financial](https://enablefin.com).

__Technologies__: Python, Django, REST APIs, GitHub.

__Objective__: Integrate GitHub with a Django application via the GitHub REST API.

__Environment setup__:

1. Setup an empty Django project on [Heroku](https://www.heroku.com/) (its free)
2. [Register](https://github.com/settings/applications/new) an oAuth application from your Github account
3. Create a dummy repository on your Github profile for this assignment - We’ll get to what you should do with this later.
4. Clone this repo and use it for versioning your work. __Don't push it back to GitHub.__ - From here on, commit, version and push everything you do to this repo. __Atleast one commit__ for each specification mentioned below.
5. Use Django 2.1.5, MySQL and Django ORM for db access.
6. Alright. You're good to go! Now implement the following specs.


__Specifications__ - _Start with the first and progress downwards_

1. I should be able to register as a user and then login to the application. Use the standard Django auth models for user management. __Keep it simple - name, username, password.__
2. After logging in, I should see a _Link GitHub account_ button. On clicking this, I should be asked to authorize your app (remember the one you created in Step 2 of setup) to access my Github account.
3. Persist my oAuth credentials in the db.
4. After I authorize, I should be provided with a list of my public repositories on Github and given an option to select one.
5. Store this selection in the db.
6. When I select one, set up web hooks on that repository that will relay any events on the repository, specifically, [pull request merged](https://developer.github.com/v3/activity/events/types/#pullrequestevent) and [code pushed](https://developer.github.com/v3/activity/events/types/#pushevent) to an URL endpoint on the Django app.
7. Create this URL endpoint that accepts the web hooks from my repo and store the event payload in the db.
8. Show me a list of all the web hooks events received from my repo in another page.
9. Test this out with the dummy repository created in Setup step 3.
10. Send us the link to your Heroku app.
11. __DONE__

__Extra__

You are free to integrate directly with the API or use one of the [suggested python wrappers](https://developer.github.com/libraries/). There are `10` suggested libraries as of this moment. Tell us why you chose the one you did.

__Reminder__: Please do not push your work into any public repositories till we tell you to.

__Good luck!__
