# Capistrano::Discord

Automatically notify a Discord channel about Capistrano deployments including new commits.

## Installation

Add this line to your application's Gemfile:

```ruby
group :development do
  gem 'capistrano-discord'
end
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install capistrano-discord

## Usage

Add to your `Capfile`

```ruby
require 'capistrano/discord'
```

You need to set the Discord API token, client ID, and the channel ID you want to notify.

```ruby
set :discord_token, "YOUR_TOKEN"
set :discord_client_id, YOUR_CLIENT_ID
set :discord_channel_id, YOUR_CHANNEL_ID
```

Additionally, the variable `local_user` lets you specify the name of whom is currently deploying.

```ruby
set :local_user, "Gabe Newell"
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/Nuke928/capistrano-discord.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

