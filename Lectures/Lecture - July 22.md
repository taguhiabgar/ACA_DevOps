## Process/PS

Tasks start processes. The task that uses CPU, HDD and RAM is a process. 
Ցանկացած գործողություն պրոցես է։

To start a process, a config file is loaded to RAM. Process has states: running, waiting, zombie, etc.

`ps -aux` (aux is for all user full) will show the processes. The process with PID=1 is init. 
`ps -ef` - same as `ps -aux`, but aux is more detailed
`ps -u username` - shows processes of the mentioned user

To view systemctl log:
`journalctl`

"**Process lifecycle**" is a topic frequently asked during the interviews.

## top/htop

`top` shows real-time process usage. `top` is more informative than `htop`.

![[Screenshot 2023-07-22 at 12.54.19.png]]
3rd line shows CPU usage percentage by user (us), system (sy), idle (id). 




