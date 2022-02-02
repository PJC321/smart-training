# External API: testing

Previously, we’ve combined background processing and connecting to an external API. It’d be good to make sure that it works as we expect, so we’ll write some tests.

Testing APIs can be tricky though. We don’t want to make real HTTP requests every single time we run tests because it’d be inefficient and expensive. What we’re going to do is to stub the API response first by using **VCR** records called **cassettes**.

If you haven’t set up your RSpec yet, you’ll need to do it now.

## Learning objectives covered

* Set up RSpec with additional libraries such as FactoryBot and Database Cleaner (only if it hasn’t been done yet)
* Set up Webmock with VCR that are commonly used when testing external APIs
* Stub an external service
* Write tests based on recorded response

## To complete this challenge, you will need to

* Install and configure RSpec. Consider installing FactoryBot and Database Cleaner as additional gems that make writing tests easier.
* Install and configure Webmock. You also want to combine it with VCR, so this library should also be added to your project.
* Write a test checking whether the code you’ve previously implemented creates a new `Movie` record with proper attributes after fetching data from the API
* Stub the HTTP request and record the API response on a VCR cassette.
* Write tests for missing parts of the asynchronous imports flow

## Resources

* https://github.com/bblimke/webmock
* https://github.com/vcr/vcr
* https://www.honeybadger.io/blog/ruby-external-api-test/
* https://www.codewithjason.com/vcr-webmock-hello-world-tutorial/
* https://relishapp.com/vcr/vcr/v/6-0-0/docs
