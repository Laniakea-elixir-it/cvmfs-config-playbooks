# cvmfs-config-playbooks
cvmfs configuration playbooks

### cvmfs-stratum0-playbook.yml 
ansible-playbook to configure cvmfs stratum0 server on infrastructure deployed through [terraform](https://github.com/Laniakea-elixir-it/cvmfs-stratum0-infrastructure)
#### dependency 
ansible >= 2.9.6
**ansible role:** 
- name: galaxyproject.cvmfs
  version: 0.2.14

### cvmfs_client.yml
ansible-playbook to configure and install cvmfs cvmfs_client
#### dependency 
ansible >= 2.9.6
**ansible role:** 
- name: galaxyproject.cvmfs
  version: 0.2.14

