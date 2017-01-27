# `awesome_print`

Make Ruby output AWESOME with [`awesome_print`](https://github.com/awesome-print/awesome_print)!

## What's So Great About `awesome_print`?

<li> Customized indentation of Ruby output!
<li> Custom colors of one output!
<li> And you can set it up for Rails!

### Why use `awesome_print`?

Basic Ruby output isn't always readable. Arrays with hashes inside end up looking like a huge jumble of text. `awesome_print` can help!

> Demo the awesomeness of this gem!


### Ruby Demo

First, make sure you have `awesome_print` installed for your computer. 

```bash 
gem install awesomeprint
```


Get printing; get awesome! Check it out in `pry`:


<img width="80%" alt="ap pry example" src="https://cloud.githubusercontent.com/assets/3254910/22387408/5ebd827c-e490-11e6-9e6f-b0fd9fcfc066.png">

### Ruby on Rails Demo 

Add to your Gemfile:

```ruby
group :development do
  # Pretty printing for console
  gem 'awesome_print'
end
```

Now you can use it in your `rails console`!

**BEFORE `awesome_print`**

<img width="80%" alt="normal User.all output" src="https://cloud.githubusercontent.com/assets/3254910/22387183/45715cfe-e48f-11e6-95b1-0151afbfc2ae.png">


**AFTER `awesome_print` :smile:**

<img width="80%" alt="awesome_print User.all" src="https://cloud.githubusercontent.com/assets/3254910/22387200/58f0feb0-e48f-11e6-9c53-d7a40bfc6a38.png">

> Caution! `ap` doens't return the value it prints, so don't try to save it as a variable.  For example, `users = ap User.all` will make `users` `nil`!

### Use it in any Ruby file (including Rails)!

You can use `awesome_print` in files, too.

```ruby
# ap_demo.rb
require 'awesome_print'
ap_options = { ruby19_syntax: true, limit: 5, color: {fixnum: :cyan, array: :yellowish}}
puts "Default awesome_print options:"
ap (1..20).to_a
puts "Custom awesome_print options:"
ap (1..20).to_a, ap_options
```

<img width="70%" alt="default ap options" src="https://cloud.githubusercontent.com/assets/3254910/22387362/10bccaec-e490-11e6-8551-19b3e3dff65e.png">

<img width="70%" alt="custom ap options" src="https://cloud.githubusercontent.com/assets/3254910/22387374/1f03be94-e490-11e6-9517-7f334011012f.png">


If you're doing this in Rails, just remember to make sure `awesome_print` is in your Gemfile.


## Resources

<li> [Github and Docs](https://github.com/awesome-print/awesome_print)
