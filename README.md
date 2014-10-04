# sea-server: 'hello world!'

Want a server written in C that is waiting to send you what you need whenever
you need it, and do it stupidly fast?

Cool, lets build it.

sea-server is based on code from [Beej's Guide to Network Programming](http://beej.us/guide/bgnet/),
and explains in depth about C socket programming.  So definitely check that out.

Steps to awesomeness:

1. Clone git@github.com:selbyk/sea-server.git
```bash
$ git clone git@github.com:selbyk/sea-server.git
$ cd sea-server
$ ls -al
```
output:
```bash
$ ls -al
total 16
drwxr-xr-x 1 selby users   78 Oct  4 17:47 .
drwxr-xr-x 1 selby users  406 Oct  4 17:10 ..
-rw-r--r-- 1 selby users    0 Oct  4 17:47 .gitignore
-rw-r--r-- 1 selby users 8078 Oct  4 17:36 Makefile
-rw-r--r-- 1 selby users 1694 Oct  4 17:45 README.md
-rw-r--r-- 1 selby users 3286 Oct  4 17:14 sea-server.c
```
2. Build the server
```bash
$ make
```
output:
```bash
$ make
g++  -g -O2 -Wall -c sea-server.cpp -o sea-server.o
g++  -g -O2 -Wall  ./sea-server.o  -o sea-server
Type ./sea-server to execute the program.
```
If you run into problems here, make sure you have the build-essentials installed.
They contain gcc, g++, make, etc. and are required to build C code. If you run
windows, let me know what you need to do to get running.

3. Run the server
```bash
$ ./sea-server
```
output:
```bash
$ ./sea-server
server: waiting for connections...
server: got connection from 127.0.0.1
server: got connection from 127.0.0.1
server: got connection from 127.0.0.1
```

Congrats, you're all set up!

Open [localhost:3490](http://localhost:3490) in a web browser or run the command
`telnet localhost 3490`, and sea-server should have a greeting waiting for you.

Don't know where this project is going, but I have some ideas if you're open to collaboration.
You can find me in #sentiment on chat.freenode.net, by e-mail, or can stalk me down any other way.

Just don't show up at my apartment at 3 AM.  Not cool, bro.

-[Selby Kendrick](http://selby.io/)
