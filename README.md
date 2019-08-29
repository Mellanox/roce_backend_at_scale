# Example of Scale-Out Ethernet fabric deployment for RoCE accelerated K8s cluster

Kubernetes pods' use of several additional high-performance network interfaces affects suitable network designs.
The solution design of scale-out a high-performance L2 network is based on the Border Gateway Protocol (BGP) with EVPN and VXLAN overlays, which are used for network virtualization. VXLAN tunnels can satisfy this L2 adjacency requirement, and EVPN serves as a standard for scale-out L2 Ethernet fabrics. VXLAN can virtualize the data center network, enabling layer 2 segments to be extended over an IP core (the underlay). EVPN is the control plane for modern VXLAN deployments, allowing VTEPs to discover each other via EVPN and exchange reachability information such as MAC and IPs across racks.

This solution is based on **Mellanox Onyx switch operating system** and supported only from Mellanox Onyx **version 3.8.1208 and above**.

# Solution logical diagram

![image2019-8-21_14-20-7](https://user-images.githubusercontent.com/29685932/63932904-d920fe00-ca60-11e9-929b-390ba96014b1.png)

# Solution physical diagram 

Spine 1 switch IP address - 10.7.214.73

Spine 2 switch IP address - 10.7.214.74

First rack Leaf switch IP address - 10.7.214.75

Second rack Leaf switch IP address - 10.7.214.76

Service rack Leaf 1 switch IP address - 10.7.214.3

Service rack Leaf 2 switch IP address - 10.7.214.9

![at scale](https://user-images.githubusercontent.com/29685932/63930381-e982aa00-ca5b-11e9-91de-08b8be0a821b.JPG)
