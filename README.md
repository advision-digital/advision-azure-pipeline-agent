# advision-azure-pipeline-agent
* Docker image for Ubuntu 20.04 with dotnet-sdk-5.0 and docker
## References for Linux 
* [Run a self-hosted agent in Docker](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops#install-docker) 
* [Install the .NET SDK or the .NET Runtime on Ubuntu](https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu#2010-)
##
docker run -v /var/run/docker.sock:/var/run/docker.sock -it advision-azure-pipeline-agent:latest /bin/bash