# Test Spree

A poor aptempt to install & customize Spree

## What did you done?

Create new Rails application

~~~bash
$ rails new test_spree
$ cd test_spree
~~~

Install Spree gems

~~~bash
$ bundle add spree
$ bundle add spree_auth_devise
$ bundle add spree_gateway
$ rails g spree:install
~~~

Setup Devise's intializer

~~~bash
$ echo 'Devise.secret_key = "342a6e8e102fc0d5f66408631cc293109be1c0e4f562b06dbf5a80b8169de4a72781807b201312fee83a1ea120c1023e10fe"' > config/initializers/devise.rb
~~~

Install multi vendor extension

~~~bash
$ echo "gem 'spree_multi_vendor', github: 'spree-contrib/spree_multi_vendor'" >> Gemfile
$ bundle install
$ rake spree_multi_vendor:sample:create # add sample data
~~~

That's it!

## How run it?

~~~bash
$ git clone https://github.com/madeindjs/test_spree
$ cd test_spree
$ bundle Install
$ rake db:migrate
$ rails server
~~~
