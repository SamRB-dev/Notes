##  Unix Processes [Source](https://lloydrochester.com/post/unix/unix-process-tutorial/)
- **Process**: The execution of a program.
- A _process_ will have an ID (pid), a parent process ID (ppid), and a process group ID (pgid).
- A process group is a collection of processes and has a pgid, a session ID (sid) to which it belongs, and will be running in the foreground or background. A single process in the process group will be the process group leader. The process group leader has the same process (pid) as the (pgid).
- The session is a collection of multiple process groups. One of the process groups will be the session leader.
- Attributes of a Process Group:
	- Foreground of Background
	- Session ID
	- The process group leader is the process where with PGID=PID
- Attributes of a Session
	- Controlling Terminal
	- The session leader is the process where the SID=PID

## Commands
```shell
ps -p $$ -o "pid ppid pgid sid command"
ps -p 2948815 -o "pid ppid pgid sid command"
```

```shell
pstree
```

## Daemon
- A process that runs on background and fully detached from controlling terminal.
- Techniques to create daemons
	- with daemon() function to create traditional bsd like daemon.
	- with systemd
	- double fork
- *fork()* in unix, is a system call that creates a new process (child).
- *Libraries*: 
	- unistd.h
	- 