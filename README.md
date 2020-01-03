## Exabgp role

This role uses https://github.com/Exa-Networks/exabgp

#### Variables

##### General

* `instances`: [optional, default: ``]: list of instances exabgp is to be installed on
* `bgp_neighbors`: [optional, default: ``]: List of bgp neighbors to advertise prefixes to
* `community_list`: [optional, default: ``]: communities to be used when advertising prefixes
* `anycast_cidrs`: [optional, default ``]: list of anycast cidrs to be advertised via bgp
