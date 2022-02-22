# cvmfs-config-playbooks
cvmfs configuration playbooks

### cvmfs-stratum0-playbook.yml 
ansible-playbook to configure cvmfs stratum0 server on infrastructure deployed through [terraform](https://github.com/Laniakea-elixir-it/cvmfs-stratum0-infrastructure)
#### dependency 
ansible >= 2.9.6  
**ansible role:**  
- name: galaxyproject.cvmfs    
  version: 0.2.14

### cvmfs-stratum1-data.galaxyproject-playbook.yml
ansible-playbook to configure cvmfs stratum1 server with the data.galaxyproject.org repository on infrastructure deployed through [terraform](https://github.com/Laniakea-elixir-it/tf-cvmfs-stratum1-refdata-GARR).  
If wanted, the GEO API license key can be added by modifying the variable `cvmfs_geo_license_key`.
#### dependency
ansible >= 2.9.6  
**ansible role:**  
- name: galaxyproject.cvmfs  
  version: 0.2.14

**Note:** when configuring a stratum1 server on an Ubuntu machine, the ansible role galaxyproject.cvmfs needs to be modified due to some missing dependencies. For the role to work on an Ubuntu machine, add `libapache2-mod-wsgi` and `squid` to the cvmfs_packages.stratum1 variable in /vars/debian.yml

### cvmfs-stratum1-data.elixir-italy-playbook.yml
ansible-playbook to configure cvmfs stratum1 server with the data.elixir-italy-cvmfs repository on infrastructure deployed through [terraform](https://github.com/Laniakea-elixir-it/tf-cvmfs-stratum1-refdata-GARR)  
If wanted, the GEO API license key can be added by modifying the variable `cvmfs_geo_license_key`.
#### dependency
ansible >= 2.9.6  
**ansible role:**  
- name: galaxyproject.cvmfs  
  version: 0.2.14

**Note:** when configuring a stratum1 server on an Ubuntu machine, the ansible role galaxyproject.cvmfs needs to be modified due to some missing dependencies. For the role to work on an Ubuntu machine, add `libapache2-mod-wsgi` and `squid` to the cvmfs_packages.stratum1 variable in /vars/debian.yml

### cvmfs_client.yml
ansible-playbook to configure and install cvmfs cvmfs_client
#### dependency 
ansible >= 2.9.6  
**ansible role:**  
- name: galaxyproject.cvmfs  
  version: 0.2.14

