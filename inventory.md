#potential inventory items

## naming format
  * [tier][type].[size]
  * ex. 2A.small would be a pivotalcf install living on open stack of a small footprint.
  
## sizing
  * to be defined later

## tiers
  * 1 heritage - org access on a pivotalcf (only org level control, no ops manager control)
  * 2 PaaS - only access to the paas level (no iaas visibility or control)
  * 3 IaaS - iaas access and up (no visibility to the metal)
  * 4 MaaS - metal and up ( i configure and control everything from real server on up ) I get a cluster of metal with a juju console targetting it.

## types
  * A OpenStack 
  * B vSphere
  * C vCloud

## Offerings

* (1) Heritage - I get an org on a pcf instance

* (2) PaaS - I get a pre-stoodup PivotalCF foundation of my very own
  * (2B) vSphere - I get a pre-stoodup PivotalCF foundation running on vSphere

* (3) IaaS - I get my own IaaS to spin up VMs, networking, etc on
  * (3A) OpenStack Org - I get my very own OpenStack Org to use however i wish
  * (3B) vSphere - I get my very own vSphere install to use however i wish
  * (3C) vCloudDirector Org - I get my very own vCloudDirector Org to use however i wish

* (4) MaaS - I get my own bare metal set of servers to do whatever i want with
