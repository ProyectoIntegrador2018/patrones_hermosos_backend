# Patrones Hermosos

Aplicación para el manejo de logística del campamento Patrones Hermosos.

[![Maintainability](https://api.codeclimate.com/v1/badges/f10a9075d0e60177285e/maintainability)](https://codeclimate.com/github/ProyectoIntegrador2018/patrones_hermosos_backend/maintainability)

## Table of contents

* [Client Details](#client-details)
* [Environment URLS](#environment-urls)
* [Da Team](#team)
* [Management resources](#management-resources)
* [Setup the project](#setup-the-project)
* [Running the stack for development](#running-the-stack-for-development)
* [Stop the project](#stop-the-project)
* [Restoring the database](#restoring-the-database)
* [Debugging](#debugging)
* [Running specs](#running-specs)
* [Checking code for potential issues](#checking-code-for-potential-issues)


### Client Details

| Name               | Email             | Role |
| ------------------ | ----------------- | ---- |
| Silvia Iliana Ramirez Ramirez | iliana.ramirez [csoftmty.org] | Client |


### Environment URLS

* **Production** - [patrones-hermosos-backend.herokuapp.com](patrones-hermosos-backend.herokuapp.com)
* **Development** - [localhost:3000](https://localhost:3000)

### Da team

| Name           | Email             | Role        |
| -------------- | ----------------- | ----------- |
| Katie Arriaga | katiearriaga [live.com] | Development, Product Owner |
| Oscar Gonzalez | osdagoso [hotmail.com] | Development, Scrum Master |
| Melissa Treviño | mely.trevic [gmail.com] | Development, Configuration Manager |
| Rubén de la Peña | ruben.dlpena [gmail.com] | Development, Project Manager |

### Management tools

You should ask for access to this tools if you don't have it already:

* [Github repo](https://github.com/ProyectoIntegrador2018/patrones_hermosos_backend)
* [Backlog](https://github.com/ProyectoIntegrador2018/patrones_hermosos_backend/projects/1)
* [Heroku](https://dashboard.heroku.com/apps/patrones-hermosos-backend)
* [Documentation](https://drive.google.com/open?id=1d96uJnjeu13aSVAOIVgP4_Rpif_TdYBF)

## Development

### Setup the development environment

First, make sure you've installed all the necessary tools.

#### For MacOS X 10.14

1. Install Homebrew

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

2. Install rbenv

```
$ brew install rbenv
$ rbenv init
```

3. Close your Terminal window and open a new one so your changes take effect.

4. Install Ruby 2.6.1

```
brew install rbenv ruby-build

# Add rbenv to bash so that it loads every time you open a terminal
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile

# Install Ruby
rbenv install 2.6.1
rbenv global 2.6.1
ruby -v
```

5. Install Rails 5.2.2

```
gem install rails -v 5.2.2
rbenv rehash
```

6. Install PostgreSQL

```
brew install postgresql
brew services start postgresql
```

7. Clone the repository into your local machine

```bash
$ git clone https://github.com/ProyectoIntegrador2018/patrones_hermosos_backend.git
```

8. Move into the project folder with `cd patrones_hermosos_backend`.

9. Install figaro locally.

```
$ bundle install
$ bundle exec figaro install
```

10. Add the database info in the generated `config\application.yml` file.

```
phb_db_host: "The host URL of the DB with quotes"
phb_db_port: "The port number of the DB with quotes"
phb_database: "The name of the database with quotes"
phb_db_username: "The username of the DB with quotes"
phb_db_password: "The password of the DB with quotes"
```

11. Setup the database's environment variables

```
$ nano .bash_profile
```

Inside the `.bash_profile` file, enter at the end:

```
export PHB_DB_HOST="The host URL of the DB with quotes"
export PHB_DB_PORT="The port number of the DB with quotes"
export PHB_DATABASE="The name of the database with quotes"
export PHB_DB_USERNAME="The username of the DB with quotes"
export PHB_DB_PASSWORD="The password of the DB with quotes"
```

12. Restart the terminal

13. Setup the database:

```
$ rails db:migrate
```

14. Start the application:

```
$ rails serve
```

#### For XXX

* Install GPG keys
\
`$ gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
* Install RVM
\
`curl -sSL https://get.rvm.io | bash -s stable`
* Install Ruby - Version 2.6.1
\
`rvm install "ruby-2.6.1"`
`rvm use ruby-2.6.1 --default`
* Install Rails - Version 5.2.2
\
`gem install rails -v 5.2.2`
* Install Postgres 11
\
Go to https://www.enterprisedb.com/downloads/postgres-postgresql-downloads.

After installing please you can follow this simple steps:

1. Clone this repository into your local machine

```bash
$ git clone https://github.com/ProyectoIntegrador2018/patrones_hermosos_backend.git
```

2. Setup the database:
```
$ rails db:migrate
```

3. Start the application:

```
$ rails s
```

### Running the stack for Development

1. Fire up a terminal and run: 

```
$ rails s
```

### Stop the project

In order to stop the project just hit Ctrl-C on the terminal where out Rails server is running.

### Deploying the project

1. The environment keys need to be setup/updated (if modified). Fire up a terminal, navigate to the project directory, and run: 

```
$ figaro heroku:set -e production -a patrones-hermosos-backend
```
