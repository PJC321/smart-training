# Tools: linters

In this challenge, you’ll set up **Rubocop** which is a static code analyzer and formatter, that helps to follow Ruby community standards in terms of syntax.

## Learning objectives covered

* Use Rubocop
* Configure own Rubocop configuration file

## To complete this challenge, you’ll need to

* Install `rubocop`, `rubocop-rails` and `rubocop-rspec`
* Generate a `rubocop_todo.yml` file so everything passes
* Create a configuration yml file and define the following cops:
* Exclude unnecessary dirs
  * Line length -> 120
  * Empty lines around class body -> enforced to no empty lines
  * No block length limit for `spec` dir
  * Context (in specs) can start only with: when, with, without, if, and
* Fix issues, so no `rubocop_todo.yml` is needed anymore
  * You can slightly automate the process by using `-a` or `-A` option

## Resources

* https://github.com/rubocop/rubocop
* https://github.com/rubocop/rubocop-rails
* https://github.com/rubocop/rubocop-rspec
