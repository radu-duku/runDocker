# wtf is this...
This is just a script that will start an  interactive bash shell by giving the container name only.

If you run the command/script without any container name you will get a list of the running containers on your system

```
#runDocker 
	To run bash in docker:

Usage: runDocker [docker image name] 		* Name is case sensitive

Here is the list with the running containers on your system:
	Name To Use                   	ID of docker Container                            
	SomeContainerName              	docker/container:latest
```

# Make it run like any other command in terminal..
**1** *Save the contetnt of the **runDocker** file, make an alias to:*

```bash
alias aliasname='/bin/bash /path/to/the/runDocker/file'
```


**2** *Save the contetnt of the **runDocker** file in one of the folder from your path*

If you save the file in */bin/*(you need root privileges) as *runDocker* because you want to run it like a normal command in your terminal,
don't forget to make it executable. 

To do this you have to run: 
```bash
chmod +x /bin/runDocker    # it may require sudo 
```

*change runDocker to what you want the command to be*

# If *bash* is not installed in the container

You can change ***bash*** from the last line to ***sh*** or another shell that you know is in the container

```bash 
docker exec -ti $1 /bin/bash
```
