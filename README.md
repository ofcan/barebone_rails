![Barebone Home](/app/assets/images/barebone_home.png)

# Barebone typical Rails app
Every app I've done in Rails has exactly the same beginning. I've decided to
make it easy on myself and have made a repo containing the code. You can see the
whole guide on my blog in the post ['How I setup my Rails
apps'](http://svenduplic.com/2012/12/22/how-i-setup-my-rails-app.html).

### Workflow

1. Clone the repo

    `git clone git@github.com:ofcan/barebone_rails.git`

2. Change the code in `.ruby-version` file to match the rvm gemset you wish to use
3. Configure your Postgresql database

    `sudo -u postgres psql`
    `create user my_app with password 'secret';`
    `create database my_app_development owner my_app;`
    `alter user my_app createdb;`
    `\q`

4. Copy database.yml.example file, rename it and configure it properly

    `cp config/database.yml.example config/database.yml`
    `vim config/database.yml`

5. Run rails server. All should be working! Happy coding! :)

    `rails s`
