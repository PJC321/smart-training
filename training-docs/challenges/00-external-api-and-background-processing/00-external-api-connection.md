# External API: connection

In this challenge, we’ll create a straightforward proxy API by adding a route that receives a movie name and returning appropriate data immediately, based on an external API called [omdbapi.com](https://omdbapi.com).
It's gonna be operating on behalf of OMDb API, passing its data on the fly so every time someone calls the endpoint they'll get data fetched from the 3rd party service.

To fetch the data we’ll use an HTTP client library responsible for HTTP requests.

## Learning objectives covered

* Define a route with a custom parameter
* Use an HTTP client

## To complete this challenge, you will need to

* Generate an OMDb API key in order to call the API
* Define a route, `get /movies/:title`. `title` is a parameter
* Install an HTTP client library of your choice. You can additionally check whether the library has a built-in parse method or you need to use [JSON](https://ruby-doc.org/stdlib-2.7.5/libdoc/json/rdoc/JSON.html).
* Set up a connection with the API. If you do it out of the `app` dir, you may want to add it to the load paths.
* Call the API any time we visit the route in the browser
* Set `Content-Type` to `json` and respond with proper HTTP status, based on whether the given movie was found or not

## Resources
* https://github.com/markets/awesome-ruby#http-clients-and-tools
* https://rubyapi.org/2.7/o/net/http
* https://www.twilio.com/blog/5-ways-make-http-requests-ruby
* [JSON Formatter - Chrome extension ](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=en)
