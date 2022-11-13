***

# Ultimative containerisation tool

![[Pasted image 20221022124225.png]]

- ## Containerisation

	 Way to collect complex of apps and their depencies in one isolated process.  

- ## Containerisation vs Virtualization

	 Difference between this two technologies is simple

	 Containerisation is Linux Core feature, and isolating process organise on the level of operating system. Container use your resources as another process

	 Virtualization organised on the hardware level, it use your cpu and ram directly.

- ## Docker image

- #### search
	 It is a  kind of template of Docker container. You can find docker images on [Docker hub](https://hub.docker.com/search?q=) Or you can use [[docker search]] command.

- #### download
	 After your choose docker image you need to download it from repository.
	 For this use [[docker pull]] command.

- #### show images
	 You can see downloaded images by command [[docker image ls]].

- #### create container
	 To create container use [[docker create]]

- #### see local containers
	 To see running containers use [[docker ps]], to see non-active use containers use -a key.

- #### rename container 
	 Use [[docker rename]]
 
- #### start container
	 To start container use [[docker start ]]

	 Or use [[docker run]] it is more powerful tool.

- #### connect to container
	 [[docker attach]] - Connect container input/output/error streams to your local terminal by using, but when you close it container will be stopped. 

	 [[docker exec]] - run a command in container

- #### get logs
	 [[docker logs]]

***

## #Docker