# turtlebot3_simulations_ansible
Ansible playbook for setting up turtlebot3_simulations packages

## Supported ROS distributions

[![noetic][noetic-badge]][noetic]
[![ubuntu20][ubuntu20-badge]][ubuntu20]

・Noetic (master)

・Humble (humble-devel is in development)

## How to use

### Execute ansible playbook
First, specify the IP address of the target(Jetson, Raspberry Pi, etc.) in the inventory.ini file.
```
[target]
192.168.11.7
```

Second, set the target name of user, password.
```
ansible_user: jetson
ansible_password: jetson
```


Finally, run the ansible-playbook command bellow.
```
ansible-playbook site.yml
```

### Confirm packages & build
After checking each package, build on the target (Jetson, Raspberry Pi, etc.) side.
```
cd ~/tb3_noetic_ws/ && catkin_make
```

## License
This repository is licensed under the Apache Software License 2.0, see LICENSE.

[noetic-badge]: https://img.shields.io/badge/-NOETIC-green?style=flat-square&logo=ros
[noetic]: http://wiki.ros.org/noetic
[ubuntu20-badge]: https://img.shields.io/badge/-UBUNTU%2020%2E04-blue?style=flat-square&logo=ubuntu&logoColor=white
[ubuntu20]: https://releases.ubuntu.com/focal/
