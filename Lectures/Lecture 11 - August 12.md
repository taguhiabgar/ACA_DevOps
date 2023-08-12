### Environment Variables

Shell communicates directly with Kernel. Kernel is the layer between application and hardware.
Applications can use environment variables to communicate with the Shell.

Command to print environment variables: `printenv`

`echo $SHELL` - print value of environment variable SHELL

`export test="hello"` create local environment variable for current user

to create a global environment variable: 
`sudo vim /etc/environment`
or with root user create environment variables for each user (???)
`vim .bashrc` - and add there command export variable

### Types of shell

- sh
- bash
- ksh
- zsh
- csh
- tcsh

to view available shells:
`cat /etc/shells`

**Learn bash scripting.**

In bash the lines are executed consecutively (one after another), if there's an error, then the execution will stop. If you want the execution to continue, you may use *set -option*. 


***script.sh (example)***
`echo "Provide your username:"`
`read name`
`echo "Nice to meet you, $name"`
`sleep 3 # sleep for 3 seconds`
`# this is a comment`


