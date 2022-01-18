# External API: securing the access key

Previously, we’ve added missing tests for asynchronous imports. We can be more confident about the implementation now as the specs cover it, but can we be sure that our implementation, or being more precise, sensitive data is safe?

In this challenge, you’ll secure your API access key and compare the 2 most common solutions in Rails apps - environment variables (by using **dotenv** or **figaro** gem) and built-in credentials. Eventually, choose one that you prefer more.

## Learning objectives covered

* Use environment variables in a Rails app
* Use Rails credentials as embedded functionality

## To complete this challenge, you will need to

* Install a gem to load environment variables
* Replace hardcoded API access key to be loaded from env vars
* Prepare an example file of environment variables
* Generate Rails credentials
  * You can generate them per environment by using `--environment` option
* Load the access key from Rails credentials
* Choose one solution you like more
* Add a different API key for the test environment

## Resources
* https://github.com/bkeepers/dotenv
* https://github.com/laserlemon/figaro
* https://guides.rubyonrails.org/security.html#environmental-security
