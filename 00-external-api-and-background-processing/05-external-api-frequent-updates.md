# External API: frequent updates

Previously, we’ve secured our API access key. Some challenges ago we’ve also implemented importing movie data asynchronously. Now we’d like to prepare frequent updates to keep e.g. IMDB score up to date.

In this challenge, we’ll run a worker every day to go through all the records and update them. To define the frequency we need to use **cron**. If we used an enterprise version of Sidekiq, such a functionality would be already available but we’ll choose a free solution.

## Learning objectives covered

* Update a huge number of records
* Use cron with periodic jobs

## To complete this challenge, you will need to

* Create a new worker updating all `Movie` records
* Install a library of your choice to set up periodic jobs
* Configure a period job that should run every day at 7am
* Don’t forget to write specs

## Resources
* https://github.com/moove-it/sidekiq-scheduler
* https://github.com/ondrejbartas/sidekiq-cron
* https://github.com/simplymadeapps/simple_scheduler
* https://github.com/javan/whenever
* https://crontab.guru/
