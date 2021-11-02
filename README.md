# Ansible Demo

This repo was created for an internal presentation on "Ansible 101: A gentle introduction"

It is not necessarily using best practices, as simplicity and ease of digestion was higher priority.

## Pre-requisutes

1. Install the galaxy roles using `ansible-galaxy install -r requirements.yaml`
1. boto3 and botocore installed on your localhost
1. Update the vars in `provision.yaml` to match your VPC, subnet etc.
1. Update the private key file in `ansible.cfg`

## Running

There are three plays here

- `povision.yaml` creates two EC2 instance from an Ubuntu AMI.
- `site.yaml` installs nginx, php and a couple of test php pages on the web server, and mysql on the database server
- `terminate.yaml` removes the two EC2 instances
