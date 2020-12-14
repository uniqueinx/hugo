---
title: "Transfer Data between pcs via ethernet cable"
date: 2020-09-09T16:28:09+02:00
draft: false
---

## Share data between two linux machines via ethernet cable

- Connect the ether cable
- manually give each pc a static ip for ex. 10.0.0.1, 10.0.0.2
- ping from on to the other to make sure connection is etablshed.
- use ssh, nfs, rsync, whatever tool you prefer for transfering.
  
  
In my arch when adding the connection via nm-applet ui on arch
connection keeps closing for some reason or some hidden param that is added by the gui. So, I use this command

```shell
 nmcli con add type ethernet con-name <connection-name> ifname enp8s0 ip4 10.0.0.1/24 gw4 10.0.0.1
```