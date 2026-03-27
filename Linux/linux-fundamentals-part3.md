

###  Text Editors
- `nano filename`
  - Simple terminal-based text editor 

- `vim filename`
  - Advanced text editor with more control and features

---

###  File Downloading

wget-
	to download file form web
	syntax- wget_URL
	ex- For example, if I wanted to download a file named "myfile.txt" onto my machine, assuming I knew the web address it -- it would 	look something like this:
			wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt

scp(secure copy)-
		Copy files & directories from your current system to a remote system.
		Copy files & directories from a remote system to your current system.

	Transfering file from
		a.my pc to remote pc
			syntax- scp myfilename.txt username@ipaddress:home/username/newfilename.txt
				ex-scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt
		b. remote pc to my pc
			syntax- scp username@ipaddress:home/username/hisfilename.txt newmyfile.txt
				ex-scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt


convert remort server in to server:-
		1.login using ssh in remote pc
		2.command is[ python3 -m  http.server ]
		3.from new terminal use wget to download files from remote pc



**Process**
ps- to see process goin in pc.
ps id - to see specific process
ps aux - to see process run by different users.
top- to see detailed processes view.
kill - to kill all process
	to kill specific PID(process id)-syntax(kill ----)
TO KILL THE PROCESS EFFICIENTLY-
	Below are some of the signals that we can send to a process when it is killed:

SIGTERM - Kill the process, but allow it to do some cleanup tasks beforehand
SIGKILL - Kill the process - doesn't do any cleanup after the fact
SIGSTOP - Stop/suspend a process

systemct1-allows us to interact with the systemd process/daemon.
	syntax:- systemctl [option] [service]
	
	-We can do five options with systemctl:

	Start
	Stop
	Enable
	Disable
	Status
	
		ex- systemctl start apache2

ctrl+z = to stop thr running process
	- also to shift process in background.

fg - to run background process in to foreground.



apt = package manager
repo = software ka source
GPG key = security check


