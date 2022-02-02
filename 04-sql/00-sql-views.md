# SQL: views
In this challenge, we’ll touch on **SQL views**. They aren’t very different from classic tables, we can consider them as virtual tables based on an SQL statement.
They have fields from one or more real tables in the database and can be useful for reusing complex queries across the application.

Before we focus on the SQL views, we need to introduce some changes in the database. We’ll create another table storing some rates, so our final result will be a query fetching data from both `movies` and `external_ratings` tables.
Then, we’ll prepare the view and display results on a page.

## Learning objectives covered

* Use scenic gem
* Create a materialized view
* Refresh a materialized view

## To complete this challenge, you’ll need to

* Create `external_ratings` table that will contain `source_name` (string) and `rating` (float). There should be an association between `external_ratings` and `movies`.
* Prepare some data to fill in the table. You can use ratings from OMDb API response. Examples of rating sources:
  * Internet Movie Database
  * MetaCritic
  * Rotten Tomatoes
* Install `scenic`
* Prepare `top_movies` materialized view (works only with Postgres) that includes
  * ID
  * Title
  * Released
  * Poster
  * Average rating
* Limit the records being returned in the view to 100
* Sort the records by rating (descending order)
* Add a link to the top movies page in the navigation bar

## Resources

* https://levelup.gitconnected.com/postgresql-views-with-ruby-on-rails-78260cd6f021
* https://pganalyze.com/blog/materialized-views-ruby-rails
* https://github.com/scenic-views/scenic
