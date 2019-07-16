# NGINX Ingress Controller Port Forward

Easily access your development pods through NGINX ingress controller with https://localhost

## Installation

Download the script:

`wget https://raw.githubusercontent.com/leandrohsilveira/ingressfwd/master/ingressfwd && chmod +x ingressfwd`

Make it available in your \$PATH:

`sudo install ingressfwd /usr/local/bin/`

## Usage

### Initialize configuration

Run `ingressfwd init` to be prompted to config:

| Config       | Description                                            | Default     |
| ------------ | ------------------------------------------------------ | ----------- |
| Namespace    | The namespace where the ingress controller is deployed | kube-system |
| Address      | The host machine IP address to accept                  | 0.0.0.0     |
| Port mapping | The port mapping expression HOST:CONTAINER             | 443:443     |

### Start port forward

Run `ingressfwd start` to start the port forward in background.

### Stop port forward

Run `ingressfwd stop`.

Enter the process ID of the `kubectl port-forward` command
