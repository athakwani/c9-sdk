This repository container dupper template for browser based development environment.

Browser Development Environment
===============================

You can setup browser based development environment for any git repository using cloud-9 sdk by running below command.

.. code-block:: bash

  # Install dupper
  curl -sSL https://get.dupper.co | sh

  # Setup cloud 9 sdk environment
  dupper dup --name=myrepo --template-from=https://github.com/athakwani/c9-sdk <YOUR_GIT_REPO_URL>
  dupper exec myrepo c9

You can also host development environment in Digital Ocean or any other cloud provider using docker-machine and dupper:

.. code-block:: bash
  
  # Install docker-machine
  curl -L https://github.com/docker/machine/releases/download/v0.7.0/docker-machine-`uname -s`-`uname -m` > /usr/local/bin/docker-machine 
  chmod +x /usr/local/bin/docker-machine
  
  # Provision ubuntu host with your access token 
  docker-machine create --driver digitalocean --digitalocean-access-token=<your access token> \
  --digitalocean-image "ubuntu-14-04-x64" devenv-node
  eval $(docker-machine env devenv-node)

  # Install dupper
  curl -sSL https://get.dupper.co | sh

  # Setup cloud 9 sdk environment
  dupper dup --name=myrepo --template-from=https://github.com/athakwani/c9-sdk <YOUR_GIT_REPO_URL>
  dupper exec myrepo c9    
