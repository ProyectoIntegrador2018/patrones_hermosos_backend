# Patrones Hermosos

Aplicación para el manejo de logística del campamento Patrones Hermosos.

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

* **Production** - [localhost:3000](https://localhost:3000)
* **Development** - [TBD](TBD)

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
* [Heroku](TBD)
* [Documentation](https://drive.google.com/open?id=1d96uJnjeu13aSVAOIVgP4_Rpif_TdYBF)

## Development

### Setup the project

First, we need to make sure we've installed all the tools we need.
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

