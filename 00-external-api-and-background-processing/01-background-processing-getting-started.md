# Background processing: getting started

Previously, we’ve added a new route where we can see movie details coming from an external API. We’ll come back to the API soon, but so far we need to set up one tool.

In this challenge, we’ll set up **Sidekiq** that makes **background processing** possible. This is an extremely useful tool, especially when we need to perform work
outside of the standard Rails request/response lifecycle. Normally, it'd be executed one by one (synchronously), but imagine that the external API responds very slowly
so it affects our response time, and we're still getting hundreds of requests to handle. To do it in a more efficient way, we need to import movies data asynchronously.
In order to obtain it, we'll create a simple worker to insert Movie records into the database.

## Learning objectives covered

* Set up Sidekiq
* Create a Sidekiq worker

## To complete this challenge, you will need to

* Set up Sidekiq with 2 queues: `default` and `movies`
* Add 1 Sidekiq process with 3 threads
* Define Sidekiq UI at `/sidekiq`
* Create `Movie` model with `title` attribute as a string
* Add a worker to create a new movie with a title given as an argument. Alternatively, you can use `faker` gem to randomise the title. The worker should use `movies` queue, without retries.
* Run the worker in your Rails console and check whether records are being created

## Resources

* https://github.com/mperham/sidekiq
* https://shashwat-creator.medium.com/all-you-need-to-know-about-sidekiq-a4b770a71f8f
