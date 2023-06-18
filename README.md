<div align="center">

<img src="https://camo.githubusercontent.com/5b298bf6b0596795602bd771c5bddbb963e83e0f/68747470733a2f2f692e696d6775722e636f6d2f7031527a586a512e706e67" align="center" width="144px" height="144px"/>

### My home Kubernetes cluster :sailboat:

_... managed with Flux and Renovate_ :robot:

</div>

<br/>

<div align="center">

[![GitHub last commit](https://img.shields.io/github/last-commit/madbuda/k3s-home?color=purple&style=for-the-badge)](https://github.com/madbuda/k3s-home/commits/main 'Commit History')
[![Release](https://img.shields.io/github/v/release/madbuda/k3s-home?style=for-the-badge)](https://github.com/madbuda/k3s-home/releases 'Repo releases')\
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white&style=for-the-badge)](https://github.com/pre-commit/pre-commit)
[![renovate](https://img.shields.io/badge/renovate-enabled-brightgreen?style=for-the-badge&logo=renovatebot&logoColor=white)](https://github.com/renovatebot/renovate)
</div>


## :book:&nbsp; Overview

This is home to my personal Kubernetes cluster. [Flux](https://github.com/fluxcd/flux2) watches this Git repository and makes the changes to my cluster based on the manifests in the [kubernetes](./kubernetes/) directory. [Renovate](https://github.com/renovatebot/renovate) also watches this Git repository and creates pull requests when it finds updates to Docker images, Helm charts, and other dependencies.

## Hardware
---
### Compute/Storage

| Device                                        | CPU          | RAM   | OS           | Disks                                                            | NICs                          |
|-----------------------------------------------|--------------|-------|--------------|------------------------------------------------------------------|-------------------------------|
| 1 x Synology DS1821+  | AMD Ryzen V1500B  | 32GB   | DSM 7.2          | 8x18TB Seagate Exos 2 x 1TB NVMe 980 Pro  SHR 114TB Usable           | 2x 10GB Mellanox ConnectX-4             |
| 1 x Open Bench Table            | i7-9700K | 64GB | Ubuntu 22.04 | 3 x 1TB NVMe Samsung 980, 1 x 1TB NVMe SPCC | Intel X710 2 x 10GB SFP+      |
| 1 x Rosewill 4U         | i7-8700 | 64GB | Ubuntu 22.04 | 3 x 1TB NVMe Samsung 980, 1 x 1TB Intel NVMe, 2x 1TB WD Blue SSD | Intel X710 2 x 10GB SFP+
| 3 x Intel NUC11TNHi70L                           | i7-1165G7    | 32GB  | Ubuntu 22.04  | 1TB NVMe Intel 1TB SanDisk SSD   | 2x I225-LM 2.5GBe |
| 3 x Lenovo M900                   | i5-6500T     | 8 GB | Ubuntu 22.04  | 1TB SPCC SSD                         |  I219-LM 1GBe  |
| 1 x Intel NUC7i7BNH                    | i7-7567U     | 8 GB | Ubuntu 22.04  | 250GB SanDisk SSD                         |  1GBe  |
| 1 x Intel NUC7i7BNH                    | i7-7567U     | 8 GB | HASSIO  | 250GB SanDisk SSD                         |  1GBe  |
| 1 x Oracle E2.1.Micro                    | x86     | 4 GB | Ubuntu 20.04   | 100GB                         | (STATUS PAGE)    |
| 1 x Oracle A1.Flex                   | 4 ARM cores     | 24 GB | Ubuntu 20.04   | 100GB                         |    |



### Networking/Other

I have a 2 gig symmetric Fiber with a /29 static IP block (only 5 usable as the gateway uses 1)

| Device                                      | Details                        |
|---------------------------------------------|--------------------------------|
| 2 x SMART1500LCD 1500VA                     | 3000VA for Servers and Storage |
| APC BE600M1 UPS                             | 600VA for UDM, GPON, and HA    |
| Unifi Dream Machine SE                      | Router / DVR / VPN to Oracle Cloud |
| USW Enterprise 8 POE                        | 2.5 GB PoE switch              |
| MikroTik CRS317-1G-16S+                     | 10GB Switch                    |
| Qnap QSW-M408S                              | Office Switch                  |
| 3 x Unifi U6-Pro                            | APs Up/Down Stairs & Garage    |
| RPI 4                                       | GPS NTP Server                 |
| Mix of G3 Flex and G4 Bullets               | security cams                  |
---

<br/>



## :handshake:&nbsp; Community

Thanks to all the people who donate their time to the [Kubernetes @Home](https://discord.gg/k8s-at-home) Discord community. A lot of inspiration for my cluster comes from the people that have shared their clusters using the [k8s-at-home](https://github.com/topics/k8s-at-home) GitHub topic. Be sure to check out the [Kubernetes @Home search](https://nanne.dev/k8s-at-home-search/) for ideas on how to deploy applications or get ideas on what you can deploy.
