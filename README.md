# ReactRailsServerRendering

Supports:

1. Rails
2. Webpack
3. React
4. Redux
5. Turbolinks
6. Server side rendering with fragment caching

# Authors
The Shaka Code team!

1. [Justin Gordon](https://github.com/justin808/)
2. [Samnang Chhun](https://github.com/samnang)
3. [Alex Fedoseev](https://github.com/alexfedoseev)

# Key Info
Currently in proof of concept phase.

1. https://github.com/justin808/react-webpack-rails-tutorial/
2. http://www.railsonmaui.com/blog/2014/10/03/integrating-webpack-and-the-es6-transpiler-into-an-existing-rails-project/
3. http://forum.railsonmaui.com
4. Lots of work to do in terms of docs, tests
5. If this project is interesting to you, email me at justin@shakacode.com. We're looking for great
developers that want to work with Rails + React with a distributed, worldwide team.


# Try it out!
Contributions and pull requests welcome!

1. Setup and run the test app. There's no database.
  ```bash
  cd spec/dummy
  bundle
  npm i
  foreman start 
  ``` 
2. Caching is turned for development mode. Open the console and run `Rails.cache.clear` to clear
  the cache. Note, even if you stop the server, you'll still have the cache entries around.
3. Visit http://localhost:3000
4. Notice that the first time you hit the page, you'll see a message that server is rendering.
   See `spec/dummy/app/views/pages/index.html.erb:17` for the generation of that message.
5. Open up the browser console and see some tracing.
6. Open up the source for the page and see the server rendered code.
7. If you want to turn off server caching, run the server like: 
   `export RAILS_USE_CACHE=N && foreman start`
8. If you click back and forth between the about and react page links, you can see the rails console
   log as well as the browser console to see what's going on with regards to server rendering and
   caching.


## References
* [Making the helper for server side rendering work with JS created by Webpack] (https://github.com/reactjs/react-rails/issues/301#issuecomment-133098974)
* [Add Demonstration of Server Side Rendering](https://github.com/justin808/react-webpack-rails-tutorial/issues/2)
* [Charlie Marsh's article "Rendering React Components on the Server"](http://www.crmarsh.com/react-ssr/)
* [Node globals](https://nodejs.org/api/globals.html#globals_global)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'react_rails_server_rendering'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install react_rails_server_rendering

## Usage

PENDING. See `spec/dummy` for the sample app. 

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake rspec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/shakacode/react_rails_server_rendering. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

