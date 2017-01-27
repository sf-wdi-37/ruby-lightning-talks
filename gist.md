# `awesome_print`

Make Ruby output AWESOME with [`awesome_print`](https://github.com/awesome-print/awesome_print)!

## Whats So Great About `awesome_print`?

<li> Customized indentation of Ruby output!
<li> Custom colors of one output!
<li> And you can set it up for Rails!

## Why use `awesome_print`?

Basic Ruby output isn't always readable. Arrays with hashes inside end up looking like a huge jumble of text. `awesome_print` can help!

## Demo the awesomeness of this gem!


### Ruby Demo

First, make sure you have `awesome_print` installed for your computer. 

```bash 
gem install awesomeprint
```


Get printing; get awesome! Check it out in `pry`:


```ruby
> require "awesome_print"
> zed = { name: "Zed", age: 37, lunch: "salad" }
> print zed
# {:name=>"Zed", :age=>37, :lunch=>"salad"}=> nil
> ap zed
# {
#             :name => "Zed",
#              :age => 37,
#            :lunch => "salad"
# }
=> nil
```

### Ruby on Rails Demo 

Add to your Gemfile:

```
group :development do
  # Pretty printing for console
  gem 'awesome_print'
end
```

Now you can use it in your `rails console`!

**before**
```ruby
irb(main):001:0> User.all
  User Load (0.6ms)  SELECT "users".* FROM "users"
=> #<ActiveRecord::Relation [#<User id: 1, email: "a@a.a", first_name: "a", last_name: "a", password_digest: "$2a$10$WuYLqapmyHZSblS1/k5qLeEQtslK9bq6vL2JoK1F9RJ...", created_at: "2016-05-17 22:33:11", updated_at: "2016-05-17 22:33:11">, #<User id: 2, email: "a@a.a", first_name: "a", last_name: "a", password_digest: "$2a$10$cqbZyfw9mcRfqPO78tFGieeBtYiXN8LGLyyeZar7M.C...", created_at: "2017-01-27 17:44:06", updated_at: "2017-01-27 17:44:06">]>
```

**after**
```ruby
irb(main):001:0> require 'awesome_print'
=> false

irb(main):003:0> ap User.all
  User Load (0.8ms)  SELECT "users".* FROM "users"
[
    [0] #<User:0x007fe9c119eb48> {
                     :id => 1,
                  :email => "a@a.a",
             :first_name => "a",
              :last_name => "a",
        :password_digest => "$2a$10$WuYLqapmyHZSblS1/k5qLeEQtslK9bq6vL2JoK1F9RJSn49iT/pnC",
             :created_at => Tue, 17 May 2016 22:33:11 UTC +00:00,
             :updated_at => Tue, 17 May 2016 22:33:11 UTC +00:00
    },
    [1] #<User:0x007fe9c119ea08> {
                     :id => 2,
                  :email => "a@a.a",
             :first_name => "a",
              :last_name => "a",
        :password_digest => "$2a$10$cqbZyfw9mcRfqPO78tFGieeBtYiXN8LGLyyeZar7M.COq9HhQN8dm",
             :created_at => Fri, 27 Jan 2017 17:44:06 UTC +00:00,
             :updated_at => Fri, 27 Jan 2017 17:44:06 UTC +00:00
    }
]
=> nil
```

### Use it in any Ruby file (including Rails)!

You can use awesome_print in files, too.

```ruby
# ap_demo.rb
require 'awesome_print'
ap_options = { ruby19_syntax: true, limit: 5, color: {fixnum: :cyan, array: :yellowish}}
puts "Default awesome_print options:"
ap (1..20).to_a
puts "Custom awesome_print options:"
ap (1..20).to_a, ap_options
```

If you're doing this in Rails, just remember to make sure `awesome_print` is in your Gemfile.


## Resources

<li> [Github and Docs](https://github.com/awesome-print/awesome_print)
