This profile is used to allow the containers to get its IP from the hosts network and copy the host ssh key.

How to use this profile:

1. Create a new profile 

  * `lxc profile create cloud-bridged`

2. Use seed to replace the #placeholder with the public ssh key 

  * `sed "s|#placeholder|$(cat ~/.ssh/id_rsa.pub)|" bridged_cloud.yml | lxc profile edit cloud-bridged`
