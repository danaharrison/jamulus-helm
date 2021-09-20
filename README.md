# jamulus-helm
A Helm chart to deploy Jamulus Server into a LoadBalancer-enabled K8S environment.

## Usage
This particular service is set up in an environment with LoadBalancer enabled, so that the Jamulus server can have its own IP assigned. At home, I'm using metallb and highly recommend it. You can just expose the port if you'd rather do without it.

This implementation just logs to emptyDir by default, but you can mount a directory for logging if needed.

### Values YAML

containerPort: the port on which Jamulus will run and the port will be exposed to the service

maxUsers: the maximum number of users able to connect to Jamulus at once

serverMessage: the message shown to the user when connecting to the Jamulus server

## Credits
Big thanks to [grundic](https://github.com/grundic) for their work on building out the Docker image. 
