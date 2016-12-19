IDCF CLI (by CloudStack API) Dockerfiles based on Alpine Linux 3.4.
---

## Images

https://hub.docker.com/r/pottava/idcf-cli/

## Available Tags

https://hub.docker.com/r/pottava/idcf-cli/tags/

### Supported tags and respective `Dockerfile` links

・latest ([versions/0.10/Dockerfile](https://github.com/pottava/docker-idcf-cli/blob/master/versions/0.10/Dockerfile))  
・0.10 ([versions/0.10/Dockerfile](https://github.com/pottava/docker-idcf-cli/blob/master/versions/0.10/Dockerfile))  

## Usage

You can read help document:  
`docker run --rm pottava/idcf-cli --help`

1. Configure IDCF API keys

Edit `~/.idcfrc` on your local machine.

```
[account]
host=${idcf_end_point}
api_key=${your_api_key}
secret_key=${secret_key}
```

2. Run this container with scripts  
`docker run --rm -it -v $HOME/.idcfrc:/root/.idcfrc pottava/idcf-cli listZones`

Or you can alias common prefix:

```
alias idcf="docker run --rm -v $HOME/.idcfrc:/root/.idcfrc pottava/idcf-cli"
idcf listVirtualMachines -t id,name,group,state
```
