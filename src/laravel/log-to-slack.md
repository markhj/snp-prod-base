[
  id: laravel-log-to-slack
  tags:
  locations:
]: #

# Log to Slack

Make Laravel's native logging system send messages to Slack. 2

First, make sure the channel you want to log to exists.

Next, set up an app at: https://api.slack.com/apps.

Add a new webhook under **Features > Incoming webhooks**.

> :information_source: A webhook is tied to a channel. You will need a new webhook for every new channel you want to post in.

Copy the entire webhook url and update your ``.env``:

````bash
LOG_CHANNEL=slack
LOG_SLACK_WEBHOOK_URL=https://hooks.slack.com/services/abcdef12345
````

Notice that ``LOG_CHANNEL`` is also changed.

# Short messages
You can hide the stacktrace and make the error message shorter in ``config/logging.php``:

````php
'slack' => [
  // ...
  'short' => true,
  'context' => false,
  // ...
]
````

# Log stacks
To combine multiple log channels together, for example to log different severities to different channels, please refer to:

https://laravel.com/docs/master/logging#building-log-stacks
