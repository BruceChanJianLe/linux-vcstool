# Linux vcstool

This repository demonstrates the usage of vcstool which is also a handy tool for ROS workspace setup.

## Installation

With ROS
```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install python3-vcstool
```

Without ROS
```bash
curl -s https://packagecloud.io/install/repositories/dirk-thomas/vcstool/script.deb.sh | sudo bash
sudo apt-get update
sudo apt-get install python3-vcstool
```

Alternatively,
```bash
sudo pip install vcstool
```

## Usage

Exporting repositories to test_ws.repo file.
```bash
# vsc export $path > $path_to_repo_files
vcs export src > src/linux-vcstool/test_ws.repos
```

Importing repos to src path.
```bash
# vsc import $path < $path_to_repo_files
vcs import src < src/linux-vcstool/test_ws.repos
```

## Reference

- https://wiki.ros.org/vcstool
- https://github.com/dirk-thomas/vcstool
