# Network Infrastructure

## IP Networks

IP ranges are documented as separate networks. Later on, other network devices
– whether physical or virtual – will connect to these networks. The end result
is a complete overview of assigned and unassigned IP addresses, a summary of
ports used, and the ability to execute a wide range of queries and automated
activities on your equipment (ping, nslookup, custom scripts, …)

## VLANs

VLANs need their own management and documentation if you want an up-to-date
overview of the correct configuration of routers and user devices VLANs are
connected to the corresponding IP networks.

## Routers

These layer 2/3 routers/switches, are ‘slotted into’ the racks already documented,
Entered for the correct units, a view of the rack is built up that also accurately
reflects the physical reality.

Similarly, you now connect the networks together via the correct ports.

```uml
nwdiag {
  network dmz {
      address = "210.x.x.x/24"

      web01 [address = "210.x.x.1"]
      web02 [address = "210.x.x.2"];
  }
  network internal {
      address = "172.x.x.x/24";

      web01 [address = "172.x.x.1"];
      db01 [address = "172.x.x.100"];
      db02 [address = "172.x.x.101"];
  }
}
```
