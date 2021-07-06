---
layout: post
title: Cluster Installation
bdate: June 28, 2021 3:30 PM
author: Harsha S. Bhat
math: false
tags:
  - Cluster
hide: false
---
![Desktop View](/images/posts/cluster.jpg "Cluster Installation")

After almost one year, to date, the installation of our cluster "MADARIAGA" 
has started in earnest. On Monday June 28 Schneider electric started the
installation of the power supply and backup unit. The work was finished on 
July 1. DELL will install the remaning components on July 5.

![Desktop View](/images/posts/clusterdesign.png "Cluster Installation"){:width="40%"}

{% include video.html id="-XZNlYe2Vns" caption="Hardware Installation" %}

TECH SPECS of **MADARIAGA**:

* 8 «CPU» nodes 
  		- 2x AMD EPYC 7702 2GHz Rome per node
  		- 64 cores per node 
  		- 1024 total cores
  		- 8GB RAM per core 
  		- 1TB RAM per node
* 3 «CPU + GPU» nodes
  		- 2x AMD EPYC 7452 2.3GHz Rome per node
  		- 64 CPU cores per node
  		- Nvidia Telsa A100 40GB RAM
  		- 6912 GPU Cores per node
* 1 «Storage» node	
  		- 2x AMD EPYC 7282 2.8GHz Rome per node 
  		- 32 cores per node 
  		- 108TB (Raid 6) Storage
* 1 «Login» node	
  		- 2x AMD EPYC 7272 2.9GHz Rome per node 
  		- 12 cores per node 
* 200 Gbps Mellanox Infiniband Switch HDR