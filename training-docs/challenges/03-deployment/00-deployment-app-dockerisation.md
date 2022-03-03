# Deployment: App dockerisation

In this challenge, we’ll dockerise our application. **Docker** is extremely useful, helps to build and manage your infrastructure. It allows you to package up an application or service with all of its dependencies into a standardised unit.

Thanks to that, we can set up the development environment much faster, run it in a more convenient way and deploy quickly.

## Learning objectives covered

* Use Docker image and build your own one
* Use Docker Compose
* Build your own Docker Compose config file
* Manage Docker containers

## To complete this challenge, you’ll need to

* Install Docker
* Define `.dockerignore`
* Create a dedicated Docker image for your application
  * Don't forget about JS dependencies
* Create `docker-compose.yml` file and configure multiple containers, including your application, Sidekiq, database and Redis
* Update `database.yml` file
* Configure environment variables accordingly

## Resources

* https://docs.docker.com/get-started/
* https://www.freecodecamp.org/news/docker-simplified-96639a35ff36/
* https://semaphoreci.com/community/tutorials/dockerizing-a-ruby-on-rails-application
