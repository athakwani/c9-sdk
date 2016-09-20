This repository container `dupper <https://github.com/athakwani/dupper>`_ template for Cloud-9 development environment SDK.

Cloud 9 Development Environment SDK
===================================

Cloud 9 SDK setup browser based development environment. You can start Cloud 9 adk for any git repository using dupper by running below commands. 

.. code-block:: bash

  dupper dup --name=myrepo --template-from=https://github.com/athakwani/c9-sdk <YOUR_GIT_REPO_URL>
  dupper exec myrepo c9
  
Dependencies
============

* build-essential 
* g++
* curl
* libssl-dev
* apache2-utils
* libxml2-dev
* sshfs 
* python2.7 
* python2.7-dev
* `c9-sdk <https://github.com/c9/core>`_
    
Commands
========

* c9
    
.. code-block:: bash

    Usage:
    dupper exec CONTAINER c9