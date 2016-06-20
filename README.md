**NOTE**: This playbook is obsolete; it was transformed into [ansible-role-awsserver](https://github.com/jreisinger/ansible-role-awsserver).

## About

Create a virtual server in AWS and setup my environment there.

## Setup

1) Remove keypair from AWS and private key from ~/.ssh

2) Set environment variables

    export AWS_ACCESS_KEY_ID='AK123'
    export AWS_SECRET_ACCESS_KEY='abc123'
    export GITHUB_TOKEN='ab12'  # for adding ssh public key

3) Check *CHECK ME* sections in `main.yml`.

4) Install role(s):

    ansible-galaxy install -r requirements.yml -p ~/ansible-roles/

If you do not wish to use private DNS (route53), VPC variable is not
needed and can be removed

Before running playbook, you will need to install and configure `boto`.

## Run

    ansible-playbook main.yml

## Connect

    ssh -i ~/.ssh/ansible-frodo jreisinger@frodo.reisingers.org
