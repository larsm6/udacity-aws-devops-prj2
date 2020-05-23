# Udagram (Udacity AWS DevOps Prj. 2)
Solution to udacity's project 2 by Lars Maertins.

Link to the solution: [Deployed Solution](http://udagr-webap-zwcqjps9hg23-481232267.us-west-2.elb.amazonaws.com)

![alt text](https://github.com/larsm6/udacity-aws-devops-prj2/blob/master/assets/Architecture.png "Lucidchart Udagram Architecture")
[Lucidchart link](https://app.lucidchart.com/invitations/accept/d9f62676-1cbd-4539-9acc-7d839de0a569)

## Usage
### Creation
In order to create the Infrastructure you can use the scripts:

```shell
./scripts/create.sh udagram-network network.yml network-parameters.json
```
In order to create your server infrastructure you can use the following as soon as the previous CloudFormation stack completed execution.
```shell
./scripts/create.sh udagram-servers server.yml server-parameters.json
```

### Updates
The WebAppGroup contains an update policy in order to terminate and relaunch the instances one by one while the service keeps working.
```shell
./scripts/update.sh udagram-network network.yml network-parameters.json
```
```shell
./scripts/update.sh udagram-servers server.yml server-parameters.json
```