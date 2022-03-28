# Import the movies CSV into the database

- Rails/Console
- Rails/Rake

You've built a Bootstrap-styled homepage displaying all the movies in the [provided CSV file](../training-data).

In this ticket, you'll import that data into your application by storing it in a [Postgres](https://www.postgresql.org/) database.

## To complete this ticket, you must:

- [ ] Install [Postgres](https://postgresapp.com/).
- [ ] [Connect](https://guides.rubyonrails.org/configuring.html#configuring-a-postgresql-database) your Rails application to your Postgres database.
- [ ] Create the database using the Rails CLI.
- [ ] Generate an appropriately-named Rails model (and associated migration) using the [Rails Command Line](https://guides.rubyonrails.org/command_line.html) with the following properties:
  - `show_type`, as a `string` that is never `null`.
  - `title`, as a `string` that is never `null`.
  - `director`, as a `string`.
  - `cast`, as a `text`.
  - `country`, as a `string`.
  - `date_added`, as a `date`.
  - `release_year`, as an `integer` that is never `null`.
  - `rating`, as a `string`.
  - `duration`, as a `string`.
  - `listed_in`, as a `text`.
  - `description`, as a `text`.
Feel free to rename the properties to follow conventions. 
- [ ] Migrate the database to update it with the new structure.
- [ ] Create a new Rake task for importing the CSV. Consider that you'll be [importing a lot of data](https://mattboldt.com/importing-massive-data-into-rails/)!
- [ ] Run the Rake task to import the CSV data into your database. Check that it worked using the [Rails Console](https://guides.rubyonrails.org/command_line.html#bin-rails-console).
- [ ] Rewrite your controller and view to use the database-backed models, instead of reading from the CSV.

## Tips
- When generating a model, you should always check (and amend) the generated migration file before running it.
- Rails applications default to using a lightweight in-memory database called `sqlite`. You won't need this any more, so you can remove references to `sqlite` from your application (for example, in the `Gemfile`).
- Since shows can only be one of two types ('Movie' or 'TV Show'), consider using a [Rails enum](https://betterprogramming.pub/how-to-use-enums-in-rails-6-87600e292476) for the show type. You may need to [generate a Rails migration](https://guides.rubyonrails.org/active_record_migrations.html#creating-a-standalone-migration) to do this!