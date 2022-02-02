# Background processing: asynchronous imports

Previously, we’ve set up Sidekiq and added a simple worker. If you remember, we’ve also set up a connection to an external API. Now, we want to combine both.

In this challenge, we’ll use the existing route, but instead of fetching data on the fly, we’ll respond with what we already have in the database. Otherwise, we’ll enqueue a worker responsible for fetching missing data to store it.

## Learning objectives covered

* Use a Sidekiq worker in real case scenario
* Store additional data from the API in the database

## To complete this challenge, you will need to
* Add additional attributes to `Movie` model, such as `year`, `released`, `runtime`, `plot`, `poster` and `imdbRating`. Consider using proper data types.
* Update the route so it returns data if the movie was found. Otherwise, it should respond with proper status and body, and enqueue a worker
* Visit the route to make sure it works well in both cases
