This gem helps dealing with Slack Webhooks, both outgoing and incoming. Incoming it will parse the 
posted body and allow you to access the values as well as make it easy to send a response back to the 
right Slack channel. 

Basic usage is:

```ruby
require 'slack_webhooks'

TODO: Get the slack_payload here. If you're running as a BOT server, parse it from the http post. 

sh = SlackWebhooks::Hook.new('hellobot', slack_payload, webhook_url)
text = "Hello #{sh.user_name}!"
sh.send(text)
```

See here for some usage examples: https://github.com/treeder/slackbots

## Building

```sh
gem build slack_webhooks.gemspec
gem push slack_webhooks
```
