## Exabgp role
[![Build Status](https://travis-ci.org/hybridadmin/ansible-role-exabgp.svg?branch=master)](https://travis-ci.org/hybridadmin/ansible-role-exabgp)

This role uses https://github.com/Exa-Networks/exabgp and can be configured to use health checks if required.

#### Variables

##### General

* `local_as`: [required]: ASN of exabgp instance
* `remote_as`: [required]: Peering ASN
* `bgp_neighbors`: [required]: List of bgp neighbors to advertise prefixes to
* `community_list`: [required]: Communities to be used when advertising prefixes

##### Health checks

* `use_healthcheck`: [optional, default false]: Whether or not to use health checks
* `anycast_cidrs`: [optional]: List of anycast cidrs to be advertised via bgp

#### Example

##### Basic example

```yaml
local_as: 65340
remote_as: 65359
bgp_neighbors:
  - ip: 10.220.50.10
    desc: "cr2"
    
community_list: "65359:500 65359:5000"

anycast_cidrs:
  - 10.220.59.188/32
  - 10.220.59.189/32
```

#### Author Information

Tinashe Chikomo
