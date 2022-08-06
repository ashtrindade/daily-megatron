<p align="center"><img src="./media/twitter-api-logo.png" width="100"></p>
<p align="center">
<a href="https://twitter.com/tododiamegatron"><img alt="Twitter Follow" src="https://img.shields.io/badge/Twitter-%40tododiamegatron-blue"></a>
<a href="https://github.com/ashtrindade/daily-megatron/blob/main/LICENSE"><img alt="MIT License" src="https://img.shields.io/apm/l/atomic-design-ui.svg?"></a>
</p>
<p align="center">
<a href="https://developer.twitter.com/en/docs/twitter-api/v1"><img alt="Twitter API v1" src="https://img.shields.io/endpoint?url=https%3A%2F%2Ftwbadges.glitch.me%2Fbadges%2Fstandard"></a>
<a href="https://www.npmjs.com/package/twitter-api-v2"><img alt="npm package - twitter-api-v2" src="https://img.shields.io/badge/npm--package-twitter--api--v2-orange"></a>
</p>

# Daily Megatron
A bot that tweets a unique video every single day.

## To run this project you will need:

- A Twitter Developer Account
- These packages:

    - `cron` to schedule the tweets
    - `twitter-api-v2` to communicate with Twitter API
    - `dotenv` to securely save your keys

**OBS:**
If you intend to make media upload using this API you will need Elevated Access.
- https://developer.twitter.com/en/portal/products/elevated
---
## Let's work

**Install the packages:**
```
npm i cron twitter-api-v2 dotenv
```

## How to use Cron
**The code:**
```
const CronJob = require('cron').CronJob

const job = new CronJob('00 30 11 * * 2-6', function(){
	console.log('Runing at 11:30 | Mon-Fri')
    // Runs every weekday (Monday through Friday)
    // at 11:30:00 AM. It does not run on Saturday
    // or Sunday.
});

job.start()
```

**Cron Ranges**
```
- Seconds: 0-59
- Minutes: 0-59
- Hours: 0-23
- Day of Month: 1-31
- Months: 0-11 (Jan-Dec)
- Day of Week: 0-6 (Sun-Sat)
```
