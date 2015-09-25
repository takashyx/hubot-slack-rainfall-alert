# hubot-slack-rainfall-alert
A rainfall alert script for hubot-slack

## Description
Post alerts on slack 30 minutes before it starts/stops raining(currently this script only supports locations in Japan).

![](https://github.com/takashyx/hubot-slack-rainfall-alert/wiki/images/preview.png)

##Installation
Go to your hubot-slack directory and run
```bash
npm install hubot-slack-rainfall-alert --save
```

##Configuration

### Required API keys
- Yahoo API key for Map API/Rainfall API (https://e.developer.yahoo.co.jp/dashboard/)
- Google API key for ShortURL (https://console.developers.google.com/project)

### Required parameters

Envs
```bash
export HUBOT_RAINFALL_ALERT_YAHOO_APP_ID=[Your yahoo app id here]
export HUBOT_RAINFALL_ALERT_GOOGLE_API_KEY=[Your google api key here]
export HUBOT_RAINFALL_ALERT_CHANNEL=[Channel name to post notifications ex: "general"]
export HUBOT_RAINFALL_ALERT_THRESH=[Notification threshold for rainfall(mm/h). ex: "0.5"]
export HUBOT_RAINFALL_ALERT_CRONTIME=[Describe how often you want to check the rainfall in cron format. ex: "0 */10 0,9-23 * * *"]
export HUBOT_RAINFALL_ALERT_LAT=[Latitude to check the rainfall. ex: "35.0000000"]
export HUBOT_RAINFALL_ALERT_LON=[Longitude to check the rainfalll. ex: "139.8000000"]
export HUBOT_RAINFALL_ALERT_LAT_FOR_MAP=[Latitude to show in the map on notifications. Recommend to set the same value as HUBOT_RAINFALL_ALERT_LAT ex: "35.0000000"]
export HUBOT_RAINFALL_ALERT_LON_FOR_MAP=[Latitude to show in the map on notifications. Recommend to set about 0.8 degree smaller value than HUBOT_RAINFALL_ALERT_LON so that you can see the incoming watery clouds in the map. ex: "139.0000000"]
export HUBOT_RAINFALL_ALERT_IMAGE_WIDTH=[Image width for the map/graph. Recommend: "500"]
export HUBOT_RAINFALL_ALERT_IMAGE_HEIGHT=[Image height for the map. Recommend: "500"]
```

## Special thanks
This script uses Yahoo APIs/Google APIs.