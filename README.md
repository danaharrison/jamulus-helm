# jamulus-helm
A Helm chart to deploy Jamulus Server into a LoadBalancer-enabled K8S environment.

## Usage
This particular service is set up in an environment with LoadBalancer enabled, so that the Jamulus server can have its own IP assigned. At home, I'm using metallb and highly recommend it. You can just expose the port if you'd rather do without it.

This implementation logs to your host's /var/log directory by default, but can all be changed in values.yaml.

## Installation

With Helm installed, open a terminal/command prompt one folder above the cloned repo, and run:

`helm install jamulus .\jamulus-helm\`

This will deploy a chart named Jamulus from the templates in the jamulus-helm folder.

### Values YAML

containerPort: the port on which Jamulus will run and the port will be exposed to the service

maxUsers: the maximum number of users able to connect to Jamulus at once

serverMessage: the message shown to the user when connecting to the Jamulus server

## Credits
Big thanks to [grundic](https://github.com/grundic) for their work on building out the Docker image. 
