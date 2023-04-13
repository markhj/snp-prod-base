[
  id: laravel-slack-messaging
  tags:
    - slack
  locations:
]: #

# Slack messaging

Start with:
````
composer require spatie/laravel-slack-alerts
php artisan vendor:publish --tag="slack-alerts-config"
````

Set up an app at: https://api.slack.com/apps.

Under Features > Incoming webhooks, add a new webhook.

# Configuration
In ``config/slack-alerts.php`` add webhooks.

````
'webhook_urls' => [
    'default' => env('SLACK_ALERT_WEBHOOK'),
    'notifications' => env('ANOTHER WEBHOOK'),
    // ... More, if you wish
],
````

# Sending
## Default channel
````
use Spatie\SlackAlerts\Facades\SlackAlert;
// ...
SlackAlert::message('Hello world!');
````

## Specified channel
````
use Spatie\SlackAlerts\Facades\SlackAlert;
// ...
SlackAlert::to('channel-name')->message('Hello world!');
````

## Emojis
````
SlackAlert::message('Hello world! :smile:');
````

All emojis: https://www.webfx.com/tools/emoji-cheat-sheet/

# Blocks

https://api.slack.com/block-kit

