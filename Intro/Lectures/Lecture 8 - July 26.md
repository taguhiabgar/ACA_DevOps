`sleep 100` - sleep for 100 seconds
read about `nice`
read about `renice`

`renice -15 ` - give priority -15 (highest priority is -20, lowest priority is 20)

Every process works either in background or in foreground.

`jobs` - to see what are the current jobs

To make a job to run in background or foreground there are these commands:
- `fg`
- `bg`

`&` at the end of a command means that the command should be running in the background.

To make a command not to output data we can write `nohup` command in the beginning of our command. Also `nohup` makes the command not dependent on the shell it was initiated from, so that when the shell is closed, the job will continue to run. The output goes to `nohup.out` file.

**Homework: How to make a script to a service? Try to make a script to a service.**

## Cron jobs, crontab

Cron is a task/job scheduler. Available units of time to set a schedule are: minute, hour, day, month, week.

read about `crontab` command

To do a job once, use `at` command:
`at HH:MM`
`atq # list all` 
`atrm # remove all` 
`atd #. Service`
`ctrl D to save and exit`
`at 15:52 -f ./test.sh`
`at 2:40 AM 072223 # run on date and time`
`at 4pm + 4 days # runs from 4 days`
`at now +5 # run from 5 hours from now`
`at 8:00 AM Sun # run on Sunday at 8:00`
`at 10:00 AM next month # ….`

(*useful tip*: use `date` command to see current time)

Also read about these commands: `atq`, `atrm`.

`systemctl status cron.service`
`systemctl status atd.service`

In `/var/log/` folder there is a log file called syslog that contains all the system log.
In `/var/log/` folder there is a log file called auth.log that contains all the authentication log.

Read about *log rotation in linux*. Interview question: *How does log rotation work?* 

To customize log rotation, there is `/etc/logrotate.conf` file.
There is also `logrotate` command.
Read about `rsyslog.service`.

Usually systemctl log file (`journal`) is the biggest log file. 
`journalctl --vacuum-size=10M` - to delete archived journalctl logs
[https://www.loggly.com/ultimate-guide/managing-journal-size/](https://www.loggly.com/ultimate-guide/managing-journal-size/)

