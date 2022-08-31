# Network settings and addresses

---
>[⬅️**back**](./README.md)
## IP addresses

Unlike the MAC address **the IP address can be changed** and is subject to the administrator's management. His work is facilitated by a
by a clear scheme of how IP addresses are assigned.

The IP address is a 32-bit number and is usually written in 4 packets of one
byte and decimal.

**Example: 32.126.33.21**

As a 32-bit number it looks like this:

| IP decimal | 32        | 126      | 33        | 21        |
|:-----------|:----------|:---------|:----------|:----------|
| Binary     | 00100000  | 0111110  | 00100001  | 00010101  |


## The two parts of an IP address

An IP address has **two parts**, one part represents the **number of a network**, i.e. a group of PCs belonging to the same organization and usually located at the same place. This part is called **Network ID** and must be the same for all PCs on the same network.

The other part is called **host ID** and is the **number of the device** (=host) in this network. The **netmask** of a network indicates which part of the IP address is the network ID and which part is the host ID (the term subnetmask is also used for the netmask).
term subnet mask is also used for the netmask).

**Examples

![net-host-id](./images/62-nw_800.png)

Where in the netmask **255** is written (or binary a 1), in the address is the network part (net-ID);   
where the netmask contains **0** (or binary 0), the address contains the host part (host ID).

## Network ID and Host ID

The **Network-ID** is the number of the network. The network part can be of different size, but must always be on the left side of the address. The
remaining numbers behind it, **the Host-ID,** are used to number the individual network devices in a certain network (e.g. PCs, printers,
smartphones... or nowadays sometimes refrigerators).

**Note.

- All devices within a network **must have the same network ID** so that they can communicate with each other.
  so that they can communicate with each other.   
  PCs with different network ID can not communicate
  communicate[^1] (try it by giving different network IDs to PCs on the same
  physical network different network IDs).

- However, all devices within this network ID must also have **different
  host IDs**, otherwise the communication won't work either.

[^1]: In order to communicate between different IP networks (different network ID)
you need a **router**.

Determine the **Network-ID** and the **Host-ID** (number of the device within
this network) at the following IP addresses.

![network-host-id](./images/63-ips_800.png)


Which of these devices (IP's) can communicate **directly** with each other?


---

## IP address classes (Classful Network)

Previously, IP addresses (0.0.0.0 to 255.255.255.255) were divided into different
ranges** the so-called **classes** (so-called *classful network**).
Although the classes have today in the practice hardly more meaning, one meets still frequently
the corresponding terms, so you should know the different address classes.
know the different address classes. A class fixes which part of the
address is the net-ID and which is the host-ID (no netmask is needed).

There are **5 classes**, which are marked with a letter of the alphabet (**A-E**)
whereas only **three classes (A-C)** are relevant for us.

The classes differ in the distribution (resp. the size) of the
network ID and the host ID.

|              | Network ID | Host ID |
|--------------|------------|---------|
| **Class A:** | 8 bit      | 24 bit  |

|              | network ID | network ID |
|--------------|------------|------------|
| **Class B:** | 16 Bit     | 16 Bit     |

|              | Net ID | Net ID | 
|--------------|--------|--------|
| **Class C:** | 24 Bit | 8 Bit  |

The subdivision can be recognized by the **first decimal number** (1st byte). From
the different sizes of the network ID and the host ID result also different sizes for the networks:

![A-B-C](./images/03-classes.png)

The number **in the foremost byte** clearly indicates the class.
- Usable addresses = **number of addresses - 2**.
- Do not use: **lowest** address = network address (address of the network).  
  **highest** address = broadcast (broadcast to everyone on the network)
- 127.x.x.x = **reserved** address, e.g. 127.0.0.1 -\> localhost (always your own computer).
  own computer).

Most IP addresses today are assigned, to government agencies, large companies, and especially to Internet providers.  
Most companies "rent" the internet connection from an internet provider and also get the necessary addresses. They then only need one or a few addresses to access the Internet from their internal network. Internally, so-called **private addresses** are used (more about this later).

An IP address with the number **32.126.33.21** says that it is a **Class A network** and thus the **first byte** is the **network ID**; this corresponds to the netmask **255.0.0**. Thus the network ID is **32** and

---
>[⬅️**back**](./README.md)