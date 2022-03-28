# Dockerise the app

## Outcomes

- Deployment/Docker

## Description

In the previous ticket, deployed your app to Heroku using Git.

In this ticket, you will deploy your app to Heroku using [Docker](https://www.docker.com/).

## To complete this ticket, you must:

- [ ] Install [Docker](https://docs.docker.com/get-started/).
- [ ] Define `.dockerignore`.
- [ ] Create a dedicated Docker image for your application.
  - Don't forget about JS dependencies.
- [ ] Create `docker-compose.yml` file and configure multiple containers, such as the application, database and so on.
- [ ] Update `database.yml` file.
- [ ] Configure environment variables accordingly.

## Tips

- The process of readying your app for deployment with Docker is called [containerisation](https://www.youtube.com/watch?v=0qotVMX-J5s) (📽️ ).
- [Here](https://www.microfocus.com/documentation/enterprise-developer/ed40pu5/ETS-help/GUID-F5BDACC7-6F0E-4EBB-9F62-E0046D8CCF1B.html) (📄 ) is why Docker is a good idea.
- [A guide by Semaphore](https://semaphoreci.com/community/tutorials/dockerizing-a-ruby-on-rails-application) on how to dockerise a Rails app.