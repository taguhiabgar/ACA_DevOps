`alias ll="ls -alh"`
`unalias ll`

To make alias permanent, write them in file `.bashrc` (or in `.profile`)
`vim .bashrc`
and add your alias there.

To make alias for all users:
`vim /etc/bash.bashrc`

### History
`history` command shows all your history
`!23` will execute your 23rd command in the list.
`!!` executes your last command.
`sudo !!` will execute the last command in sudo mode.

