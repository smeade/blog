# Blog

This will be a starter, demonstration and reference application which does almost nothing useful. Intention is to create a blogging app with Posts in order to have something to work with while documenting experiences with generic features used in almost all apps.

**Live Demo**

There's not much to see here yet:

https://blog2018.herokuapp.com

**Done**

This app demonstrates:
* Rails 5.x
* PostgreSQL

**To Do**

Consider implementing support for:

* Bootstrap 4
* Bootstrap themeing
* Deployment to Heroku
* Devise for authentication
* Sendgrid for transactional emails
* Etc...

Getting Started
---------------

### Deploy to Heroku
See [Getting Started with Rails 5.x on Heroku](https://devcenter.heroku.com/articles/getting-started-with-rails5).

To deploy to and run on Heroku, your app must:

- [x] use Postgres database
- [x] declare all dependencies in your Gemfile
- [x] have a root route
- [x] be stored in git

Rails 5 no longer requires the `rails_12factor` gem.

Create an app on Heroku

    $ heroku create blog2018
    Creating ⬢ blog2018... done
    https://blog2018.herokuapp.com/ | https://git.heroku.com/blog2018.git

Verify that the remote was added to your project

    $ git config --list | grep heroku
    remote.heroku.url=https://git.heroku.com/blog2018.git
    remote.heroku.fetch=+refs/heads/*:refs/remotes/heroku/*

Deploy your code:

    $ git push heroku master

Migrate your database:

    $ heroku run rake db:migrate

Visit your app:

    $ heroku open

View the logs

    $ heroku logs -t

Additional Notes and Background
-------------------------------
### Versions
* Ruby version 2.5.0
* Rails version 5.2.0


