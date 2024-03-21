title to change the title of a windows cmd prompt
```
>title hacked
```

prompt to change the prompt
```
>prompt {Practice}$G
```

color to change color 
```
>color 06
```

Windows terminal can be cleared using the command
```
>cls 
```

# Netstat
A command-line network utility that displays network connections for TCP, routing tables, and a number of network interface and network protocol statistics.

Basic command for netstat that shows the basic connections 
```
netstat 
```

See all connections and listening ports.
```
netstat -a
```

More information about netstat can be found by typing 
```
netstat /?
```

Command that shows the name of the established connections
```
netstat -b
```

<h3> By Far my favorite command to run would be </h3>
```
netstat -o -b -a
```
Because this allows me to find all information, and see the name of the services running
# NET
More information about net can be found by using the command 
```
net help
```

Information about what devices to use the command on can be found by running the command 
```
net statistics
```

The only device I could gather statistics from was called workstation prompting me to find out more by typing 
```
net statistics workstation
```

This command sees all servicing running on your system
```
net start
```


# Linux Side

Command that shows all the users ids 
```
id
```

Command to switch to a root user 
```
sudo su root
```
to exit just type exit 

Check directory using 
```
pwd
```

To switch to root directory that has full access to every directory simply type
```
sudo su -
```