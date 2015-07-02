#potential inventory items

## naming format
  * [tier][type].[size]
  * ex. 2A.small would be a pivotalcf install living on open stack of a small footprint.
  
## sizing
  * 2C.small - 128GB ram / 250GB storage / 2 routable IPs 

## tiers
  * 1 heritage - org access on a pivotalcf (only org level control, no ops manager control)
  * 2 PaaS - only access to the paas level (no iaas visibility or control)
  * 3 IaaS - iaas access and up (no visibility to the metal)
  * 4 MaaS - metal and up ( i configure and control everything from real server on up ) I get a cluster of metal with a juju console targetting it.

## types
  * A OpenStack 
  * B vSphere
  * C vCloud
  * D Raw
  * E JuJu

## Offerings

* (1) Heritage - I get an org on a pcf instance

* (2) PaaS - I get a pre-stoodup PivotalCF foundation of my very own
  * (2C) vCloud - I get a pre-stoodup PivotalCF foundation running on vCloud

* (3) IaaS - I get my own IaaS to spin up VMs, networking, etc on
  * (3A) OpenStack Org - I get my very own OpenStack Org to use however i wish
  * (3C) vCloudDirector Org - I get my very own vCloudDirector Org to use however i wish

* (4) MaaS - I get my own bare metal set of servers to do whatever i want with
  * (4D) Raw metal - i get some servers
  * (4E) Raw metal + JuJu - i get some servers targeted by the juju console to configure however i want

## possible inventory object structure
```
inventory
{
 sku: 2C.small,
 guid: kaasd9sd9-98239h23h9-99h3ba993ba9h3ab,
 tier: 2,
 type: C,
 size: small,
 attributes: [
  vCloud,
  PivotalCF,
  128GB ram,
  250GB storage,
  2 routable IPs,
 ]
 lease-guid:917397-292735-98293752935
}

lease
{
  guid: 917397-292735-98293752935,
  inventory_guid: guid: kaasd9sd9-98239h23h9-99h3ba993ba9h3ab,
  user: dnem,
  lease_status: active #[rebuilding, leased, available, maintenance, archiving], 
  lease_duration: 14 #days
  lease_end_date: 92986228624 #epoch
  lease_start_date: 73682725283 #epoch
}

```
