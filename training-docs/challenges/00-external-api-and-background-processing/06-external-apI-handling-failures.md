# External API: handling failures

So far, we’ve implemented creating and updating records, based on the API response. Unfortunately, not every time the response can be successful, so we should be ready for such cases as well.

Notice, that the response contain `response` key defining whether the request succeeded or failed. We want to know about it so we’ll write a proper message into the logs when it failed.

It may also happen, that a movie has been deleted from the API’s database and it no longer exists. In this way, some of our database records won’t be updated, so we’ll delete them as well after 48 hours.

## Learning objectives covered

* Operate on a bigger scope of records
* Distinguish record’s timestamp changes
* Use Rails logger
* Test freezing time

## To complete this challenge, you’ll need to

* Store a message of your choice in the logs when a given movie title wasn’t found in API. The message should contain the current timestamp and have the log level as a warning.
* Create a new worker deleting all `Movie` records that weren’t updated within the last 48 hours
* Run the worker frequently (every day at midnight)
* Test the log message. If it doesn’t work, look for how to freeze time in specs.

## Resources

* https://api.rubyonrails.org/classes/ActiveSupport/Testing/TimeHelpers.html
* https://github.com/travisjeffery/timecop
* https://engineering.freeagent.com/2021/03/25/timecop-vs-rails-timehelpers/
* https://guides.rubyonrails.org/debugging_rails_applications.html#the-logger
