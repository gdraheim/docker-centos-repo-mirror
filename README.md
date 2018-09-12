# docker centos-repo mirror

This docker image can be startet as a container
and it can serve as a replacment for the standard
http://mirrorlist.centos.org

When there is a mirror-query then it will answer
with an URL pointing back to the docker container.

    ORIG: http://mirrorlist.centos.org/?release=7&repo=os&arch=x86_64
    HERE: http://172.22.0.2/?release=7&repo=os&arch=x86_64
    Answered Mirrorlist:
       http://172.22.0.2/7/os/x86_64

In that way it can serve as an endpoint for another
container requiring yum packages from the central
operation system install repositories.

# superseded by new project

https://github.com/gdraheim/docker-mirror-packages-repo

The new project creates mirror images for other Linux
distributions as well. So opensuse zypper and ubuntu
apt-get can install packages from a local repo container
as well. Again it can be done without changing the 
preinstalled repo descriptors.

Tested repos are

 * localhost:5000/mirror-packages/centos-repo:7.3.1611 (17.3GB)
 * localhost:5000/mirror-packages/centos-repo:7.4.1708 (13.2GB)
 * localhost:5000/mirror-packages/centos-repo:7.5.1804 (14.7GB)
 * localhost:5000/mirror-packages/opensuse-repo:15.0   (48.9GB)
 * localhost:5000/mirror-packages/opensuse-repo:42.3   (38.6GB)
 * localhost:5000/mirror-packages/ubuntu-repo:16.04    (74.7GB)
 * localhost:5000/mirror-packages/ubuntu-repo:18.04    (19.5GB)
 * localhost:5000/mirror-packages/ubuntu-repo/universe:16.04 (186GB)
 * localhost:5000/mirror-packages/ubuntu-repo/updates:16.04 (74.7GB)
 * localhost:5000/mirror-packages/ubuntu-repo/updates:18.04 (19.5GB)
