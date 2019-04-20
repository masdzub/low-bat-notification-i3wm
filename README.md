# low-bat-notification-i3wm

Some things to note:

Line 3: the threshold percentage is configurable
Line 7: the script will exit if it’s already running to avoid multiple notifications e.g. when run by Cron
Line 11: for greater accuracy, the percentage is calculated based on the last full charge of the battery instead of its nominal capacity (the difference between the two grows as the battery gets old)
Line 17: a notification is shown using notify-send (ships with libnotify-bin on Debian)
I run the script once every minute with Cron:

```* * * * * bash /home/agorf/work/dotfiles/scripts/batmon.sh```
