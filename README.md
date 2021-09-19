# jamulus-helm
A Helm chart to deploy Jamulus Server into a LoadBalancer-enabled K8S environment.

## Usage
This particular service is set up in an environment with LoadBalancer enabled, so that the Jamulus server can have its own IP assigned. At home, I'm using metallb and highly recommend it. You can just expose the port if you'd rather do without it.
