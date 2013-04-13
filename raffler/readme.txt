casts 352 backbone-on-rails


rails new raffler
rails g controller main index --skip-javascripts

gem 'backbone-on-rails'


```
rails g backbone:install

      create  app/assets/javascripts/models
      create  app/assets/javascripts/collections
      create  app/assets/javascripts/routers
      create  app/assets/javascripts/views
      create  app/assets/templates
      create  app/assets/javascripts/raffler.js.coffee
      insert  app/assets/javascripts/application.js
```
```
rails g backbone:scaffold entry

      create  app/assets/javascripts/models/entry.js.coffee
      create  app/assets/javascripts/collections/entries.js.coffee
      create  app/assets/javascripts/routers/entries_router.js.coffee
      create  app/assets/javascripts/views/entries
      create  app/assets/javascripts/views/entries/entries_index.js.coffee
      create  app/assets/templates/entries
      create  app/assets/templates/entries/index.jst.eco
```

```
rails g resource entry name winner:boolean --skip-javascripts

      invoke  active_record
      create    db/migrate/20130413065155_create_entries.rb
      create    app/models/entry.rb
      invoke    test_unit
      create      test/unit/entry_test.rb
      create      test/fixtures/entries.yml
      invoke  controller
      create    app/controllers/entries_controller.rb
      invoke    erb
      create      app/views/entries
      invoke    test_unit
      create      test/functional/entries_controller_test.rb
      invoke    helper
      create      app/helpers/entries_helper.rb
      invoke      test_unit
      create        test/unit/helpers/entries_helper_test.rb
      invoke    assets
      invoke      coffee
      invoke      scss
      create        app/assets/stylesheets/entries.css.scss
      invoke  resource_route
       route    resources :entries

```

```
rake db:migrate
==  CreateEntries: migrating ==================================================
-- create_table(:entries)
   -> 0.0030s
==  CreateEntries: migrated (0.0032s) =========================================
```


```ruby db/seeds.rb
Entry.create!(name:'Matz')
Entry.create!(name:'Yehuda Katz')
Entry.create!(name:'DHH')
Entry.create!(name:'Jose Valim')
Entry.create!(name:'Dr Nic')
Entry.create!(name:'John Nunemaker')
Entry.create!(name:'Aaron Patterson')


```
```
rake db:seed
```
