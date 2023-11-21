Lesson-1 homework

- Spin up 3 virtual machines  (Ubuntu 22.04 or 20.04) in the same local network
	- 2 virtual machines  should act as web servers (install `nginx`) serving index.html which should contain the virtual machine’s hostname
	- 1 virtual machine (Ubuntu 22.04 or 20.04) should acts as LB in (install `nginx`)  front of 2 virtual machines
	- domain name should be `[aca.examle.com](http://aca.examle.com/)`
	- you can add the content into the index.html file doing something like this
		- `echo "<h1>Hello World from $(hostname -f)</h1>" > index.html`
