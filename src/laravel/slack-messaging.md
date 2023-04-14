[
  id: laravel-slack-messaging
  tags:
    - slack
  locations:
]: #

# Slack messaging

Start with:
````bash
composer require spatie/laravel-slack-alerts
php artisan vendor:publish --tag="slack-alerts-config"
````

Set up an app at: https://api.slack.com/apps.

Under Features > Incoming webhooks, add a new webhook.

> :information_source: A webhook is tied to a channel. You will need a new webhook for every new channel you want to post in.

# Configuration
In ``config/slack-alerts.php`` add webhooks.

````php
'webhook_urls' => [
    'default' => env('SLACK_ALERT_WEBHOOK'),
    'notifications' => env('ANOTHER WEBHOOK'),
    // ... More, if you wish
],
````

# Sending
## Default channel
````php
use Spatie\SlackAlerts\Facades\SlackAlert;
// ...
SlackAlert::message('Hello world!');
````

## Specified channel
````php
use Spatie\SlackAlerts\Facades\SlackAlert;
// ...
SlackAlert::to('channel-name')->message('Hello world!');
````

# Emojis
https://www.webfx.com/tools/emoji-cheat-sheet/

# Blocks

https://api.slack.com/block-kit

