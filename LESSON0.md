# Cron Jobs

## What is Cron Job?
The [cron](https://en.wikipedia.org/wiki/Cron) command-line utility, also known as cron job, is a job scheduler on a Unix-like operating system. Users who set up and maintain software environments use cron to schedule jobs (commands or shell scripts) to run periodically at fixed times, dates, or intervals. It typically automates system maintenance or administration—though its general-purpose nature makes it useful for things like downloading files from the internet and downloading email at regular intervals.


## Cron Job’s Use Cases
as we mentioned in the intro, there are many common use cases for using cronjob like:

- send out daily newsletter e-mails.
- backup databases on any cloud storage. to monitor the status of the server and services (internally + externally) [every 10min for example].
- Send a birthday email every year for each member.

## Cron Job Schedule Expressions
A cron job is defined by using a series of asterisks (*****) which denotes different timing as indicated below.
```
# ┌───────────── minute (0 - 59)
# │ ┌───────────── hour (0 - 23)
# │ │ ┌───────────── day of the month (1 - 31)
# │ │ │ ┌───────────── month (1 - 12)
# │ │ │ │ ┌───────────── day of the week (0 - 6) (Sunday to Saturday)
# │ │ │ │ │                                   
# │ │ │ │ │
# │ │ │ │ │
# * * * * *
```

Check [crontab guru](https://crontab.guru/) a quick and simple editor for cron schedule expressions

## Examples Of cron-job in a GNU system
The following command runs the `./clean_file.sh` script file regularly at 1 minutes past midnight everyday
```sh
1 0 * * * ./clean_file.sh
```
**More Examples of cron job notation**
- `45 23 * * 6` runs on Saturdays at 23:45 (11:45pm)
- `0 0 25 12 *` runs at midnight on 25th of December (Christmas day)
- `0 0 * * *` runs at midnight everyday
- `* * * * *` runs every minute
- `* 10,14 * * *` runs everyday at 10:00 (10am) and 14:00 (2pm)
- `0 0 14 2 *` runs every 14th day in February and at midnight

## Cron Job with NodeJS
Check [Node Cron](https://www.npmjs.com/package/node-cron) take your time and feel free to create your own example!