# azure-devops-agent
Azure Pipelines self-hosted agent to run inside Ubuntu container based on this instruction https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops

This agent comes with the below roles
 - Docker: make sure you do the below as the advice from this thread [here](https://forums.docker.com/t/how-can-i-run-docker-command-inside-a-docker-container/337/12)
	 - add `-v /var/run/docker.sock:/var/run/docker.sock` into docker run command before running this container
	 - after the container started: run this command `chown -R root:root /var/run/docker.sock` where root is the user in the container
 - dotnet: to be added