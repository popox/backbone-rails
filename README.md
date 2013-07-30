# backbone-rails

Developing javascript applications on top of rails just got faster thanks to the Rails 3.1 asset pipeline.
Like [jquery-rails](https://github.com/indirect/jquery-rails/), this gem bundles some javascript files to make them available to your application:

I simply added the backbone_datalink from rails-backbone gem in order the get an easier binding between forms and models.

* [backbone](http://documentcloud.github.com/backbone)
* [backbone_datalink](https://github.com/codebrew/backbone-rails/blob/master/vendor/assets/javascripts/backbone_datalink.js)
* [underscore](http://documentcloud.github.com/underscore)
* [json2](https://github.com/douglascrockford/JSON-js)

## How to use it

### Rails 3.1

Add it to your Gemfile:

    gem 'backbone-rails', :git => 'https://github.com/popox/backbone-rails.git',:branch => 'v1.1'

Require backbone and its dependencies as a group in `app/assets/javascripts/application.js.coffee`:

    #= require backbone-rails

With pure javascript, the lines would look like `app/assets/javascripts/application.js`:

    //= require backbone-rails

Or if you need to, require what you need in `app/assets/javascripts/application.js.coffee`:

    #= require json2
    #= require underscore
    #= require backbone
    #= require backbone_datalink

With pure javascript, the lines would look like `app/assets/javascripts/application.js`:

    //= require json2
    //= require underscore
    //= require backbone
    //= require backbone_datalink

### Rails 3.0

`backbone-rails` ships with a generator that copies all javascript files to `public/javascripts`. You can run it with `rails g backbone:install`.

## Versioning

The gem will follow backbone versioning.

## Contributors

* [John Bintz](https://github.com/johnbintz) (Support for Rails 3.0 via generators)
* [Wes Gibbs](https://github.com/wgibbs) and [Les Hill](https://github.com/leshill) (Include all dependencies as a group)
