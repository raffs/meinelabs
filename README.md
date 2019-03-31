# Meine Labs

Meine labs is a variaty of infrastructure and devops-like tools running on
docker containers in order to be used as development and/or testing environment.
Whether you want to test new technologies, create a local instance of the services for
testing or you want to use to learn about this services, and how they maybe be
integrated with each other.

## Minimal Configuration

If you are looking for a minimal setup, use the `minimal` branch. The intent of
the `minimal` branch is to use the minimal require configuration for the service
to be sucessfully provisioned without any additional information. You can use the
minimal environment when you want test your own setup, or learn how to configure
the services for yourself.

## Available Services

Current this project contains the following services

- mysql
- postgres
- memcached
- redis
- vault
- jenkins
- gitlab
- elasticsearch
- logstash
- kibana
- grafana

You can start one service by running `docker-compose up -d <SERVICE_NAME> <SERVICE_NAME> ...`.
The `docker-compose.yml` contains more information about the service definition, where you
can find the services listening ports, volumes and variables defined during the service
deployment.

## CONTRIBUTING

Feel free to contribute with this project by opening Issue for bug fixes and improvments, or by
dive into the configuration and through Pull Requests. 

### Development Guide

If you are interested in contributing with this project, here's a simple guideline for the development
workflow. 

#### Adding a new service

In the effort to maintain a clean branch with `minimal` require installation for the service. the addition
of new services should start on the minimal branch and when it's ready move to the master branch with more
advanced configuration.

Here's a simple workflow reference for adding a new service to meinelabs

1. Create a branch from the `minimal` branch with your github name and service (i.e: github_name/my_awesome_service) 
2. Once the new service is created with a minimal configuration to sucessfully run, open a pull request for the branch
   against the `minimal` branch.
3. Once the Pull Request is approved and merge, the changes will add into the `master` branch. 
4. From now own you can use the existing service guideline to continuing improving the added service

#### Using existing service

1. Create branch from the `master` branch with your github name and service (i.e: github_name/awesome_service)
2. Once the configuration is ready, and possibily integration with other existing meinelabs service, open a Pull Request
   to merge your changes and configuratoin.

