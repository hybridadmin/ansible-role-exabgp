## Exabgp role
[![Build Status](https://travis-ci.com/hybridadmin/ansible-role-exabgp.svg?branch=master)](https://travis-ci.com/hybridadmin/ansible-role-exabgp)

This role uses https://github.com/Exa-Networks/exabgp and can be configured to use health checks if required.

#### Installing the role
```
sudo ansible-galaxy install hybridadmin.exabgp
```

#### Variables

##### General

* `local_as`: [required]: ASN of exabgp instance
* `remote_as`: [required]: Peering ASN
* `bgp_neighbors`: [required]: List of bgp neighbors to advertise prefixes to
* `community_list`: [optional]: Communities to be used when advertising prefixes
* `anycast_procs`: [optional]: List of anycast cidrs to be advertised via bgp

#### Example

##### Basic example

```yaml
local_as: 65340
remote_as: 65359
bgp_neighbors:
  - { ip: 10.220.50.10, desc: "cr2" }
    
community_list: "65359:500 65359:5000"
anycast_procs:
  - name: dns1v4
    cidr: 192.168.59.188/32
  - name: dns2v4
    cidr: 192.168.59.189/32
```

#### Author Information

hybridadmin
