# lab_driver

## Overview
This was creates to host the main CLI ansible driver for testing the lab_base and lab_server ansible roles.  Eventually I will find a gui that makes me happy.
Until then, this is a good way to get started.

## ansible.cfg
Creeting a local config file allows me to specify and inventry and leave it off the command line.

Also added in some extra confguraitons to profile the tasks and allow pipeliine

And very handy is to add in a "specific" ssh rsa token to support sending in the sudo password key.

`ssh_args = -i worker/id_rsa`

To make this usable I did an ssh-keygen this directory to a folder named "work".  Then I copied the key to each item in the inventory

`ssh-copy-id -i worker/id_rsa.pub lavender@192.168.38.12`

Note: I require a password for the remote user to get sudo.  Currently I am limited to useing a single password for sudo.  I hope to remove over time.

From the command line I can test the process by

`ansible-playbook first.yml -K`

and give the password on the command line.  This decouple sudo from ssh.

``

## inventory

Using YAML.  This allows me to use differet users on each machine. As well as add machines to roles.  





## Misc


### Meaningless task list

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media



