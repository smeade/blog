# Blog

This will be a starter, demonstration and reference application which does almost nothing useful. Intention is to create a blogging app with Posts in order to have something to work with while documenting experiences with generic features used in almost all apps.

**Live Demo**

There's not much to see here yet:

https://blog2018.herokuapp.com

This app demonstrates how to:

- [x] Rails 5.x
- [x] PostgreSQL
- [x] Deployment to Heroku
- [ ] Integrate Bootstrap 4
- [ ] Theme Bootstrap 4
- [ ] Authenticate via Devise
- [ ] Manage accounts and teams
- [ ] Send transactional emails with SendGrid
- [ ] Build a pricing and plan selection page
- [ ] Accept payments and subscriptions via Stripe
- [ ] Integrate Google Analytics/Mixpanel/Segment/etc
- [ ] Etc...

Getting Started
---------------
### Install Dependencies

#### Rails 5.x

If you do not yet have Rails 5.x installed, follow the [Getting Started Guide](http://guides.rubyonrails.org/getting_started.html) to [install Rails 5.x](http://guides.rubyonrails.org/getting_started.html#installing-rails). I recommend using [rvm](https://rvm.io).

#### Postgres

In order to deploy to Heroku, this project uses PostgreSQL.

### Clone, configure and run locally

1. Clone the project:

        git clone git@github.com:smeade/blog.git
        cd blog

2. Install gems:

        bundle install

3. Create, migrate and seed the database:

        rake db:create db:migrate db:seed

4. Start the web server:

        rails server

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


