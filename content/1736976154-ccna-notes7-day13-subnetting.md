---
id: 1736976154-ccna-notes7-day13-subnetting
aliases:
  - ccna-notes7-day13-subnetting
tags: []
---

# ccna-notes7-day13-subnetting

CIDR (Classless Inter-Domain Routing)
![1736980766-ipv4-address.png](assets/1736980766-ipv4-address.png)
[[ccna-notes2]]
- Class A
0.0.0.0 ~
127.255.255.255
    - Prefix /8
- Class B
128.0.0.0 ~
191.255.255.255
    - /16
- Class C
192.0.0.0 ~
223.255.255.255
    - /24
- Class D
224.0.0.0 ~
239.255.255.255
- Class E
240.0.0.0 ~
255.255.255.255
![1736981114-numberof-networks.png](assets/1736981114-numberof-networks.png)
![1736981364-wasted-ipv4.png](assets/1736981364-wasted-ipv4.png)
- wasted ip address
Company X needs IP addressing for 5000 end hosts.
A class C network does not provide enough addresses, so
lass B network must be assigned.
This will result in about 60000 addresses being wasted.

- CIDR => replace the class
Class A = /8
Class B = /16
Class C = /24

This allowed larger networks to be split into smaller networks, allowing greater efficiency.

These smaller networks are called ‘subnetworks’ or
‘subnets’

2^n - 2 = usable address
n = number of host bits
![1736982024-cidr.png](assets/1736982024-cidr.png)
![1736982148-cidr-2.png](assets/1736982148-cidr-2.png)
- 2^7+2^6 => 192
- /26 -> 32-26 = 6(1 bytes got 2 1 1 in the first)

2^6-2 = 62 usable addresses

205.90.113.0/30
= 203.0.113.0 - 203.0.113.3

.00000000
.00000001 -> we use
.00000010 -> we use
.00000011

The remaining addresses in the 203.0.113.0/24 address block
(203.0.113.4 - 203.0.113.255) are now available to be used
in other subnets!

/31 
-> replacing the 0 and broadcast addresses
=> use it only if point to point access

/32
static route => specific host only , but not network

CIDR 
![1736983316-cidr-notatino.png](assets/1736983316-cidr-notatino.png)
Case:

45 hosts per switch , 
4 switch in Total
plus the 0 and broadcast addresses, +2

47*4=188

2^6-2=62 usable address (/26)

![1736984068-quig.png](assets/1736984068-quig.png)
![1736984089-ans.png](assets/1736984089-ans.png)
subnet 2 => one bit higher than broadcast address

64
![1736984175-ans2.png](assets/1736984175-ans2.png)
subnet 3 => 10000000
11000.0.0.0.10101000.00000001.1000000
192 . 168 . 1 . 128

11000.0.0.0.10101000.00000001.10111111

192 : 168 . 1 . 191
![1736984388-ans3.png](assets/1736984388-ans3.png)
![1736984422-ansforall.png](assets/1736984422-ansforall.png)
# Subnetting trick:

just need to add 64 to find next subnetting 

 ![1736984502-sub-trick.png](assets/1736984502-sub-trick.png)
![1736984639-borrowing.png](assets/1736984639-borrowing.png)

Now we need to borrow 5 subnet in the Case

borrowing 3 bits => 8 subnets

=> 192.168.255.0/27(borrowing 3)
- use the trick ❌

**32** | 16 8 4 2 1

![1736984997-subnetting-q2.png](assets/1736984997-subnetting-q2.png)

Subnet 6: 192.168.255.160/27 - not used
Subnet 7: 192.168.255.192/27 - not used
Subnet 8: 192.168.255.224/27 - not used



- What subnet does host 192.168.5.57/27 belong to?


Subnet ID: /27

only got 192.168.5.57(pc)
![1736985157-identify-the-subnet.png](assets/1736985157-identify-the-subnet.png)
![1736985525-identify2.png](assets/1736985525-identify2.png)
11011011 -> 

What subnet does host 192.168.29.219/29 belong to ?

Subnet ID: 192.168.29.216/29

table
![1736985754-classC-subnets-table.png](assets/1736985754-classC-subnets-table.png)

# Subnetting Class B Networks

You have been given the 172.16.0.0/16 network. You are asked to create 80 subnets for your company’s various LANs. What prefix length should you use?

172.16.0.0/16

You have been given the 172.22.0.0/16 network. You are required to divide the
network into 500 separate subnets. What prefix length should you use?
172.22.0.0/16
Borrowing 9 bits= 512 subnets

![1736988855-classBq.png](assets/1736988855-classBq.png)

Borrowing 8 bits = 256 subnets (2^x)
2^8 => subnets

8 host bits = 254 hosts per subnet
(2^8-2) , host number


---

Question ❌


What subnet does host 172.25.217.192/21 belong tﬂ

Subnet ID: /21

![1736989801-ans-2.png](assets/1736989801-ans-2.png)

ans 172.25.216.0
- forget about the host for subnet

![1736991471-host&bit.png](assets/1736991471-host&bit.png)


- cal subnet first
    - cal host 

9 host bits = 2^9 - 2 = 510 usable addresses

What is the broadcast address of the network 192.168.91.78/26 belongs to?
- instead of change it to all 0 , you change it to all 1

ans: Broadcast address: 192.168.91.127 /26

Quiz:
You divide the 172.16.0.0/16 network into 4 subnets of equal size.
Identify the **network and broadcast addresses** of the second subnet.

- Borrow 2 bits = 2*2 = 4 subnets
![1736991985-damn.png](assets/1736991985-damn.png)

- /18 case

![1736992010-.png](assets/1736992010-.png)


- Quiz
You divide the 172.30.0.0/16 network into subnets of 1000 hosts each. How many subnets are you able to make?

- 10 host bits = 2^10- 2 = 1022 hosts

32 -10-16=6 
2^6 = 64 subnets

---
# Class A subnet


You have been given the 10.0.0.0/8 network. You must create 2000 subnets which
will be distributed to various enterprises.
What prefix length must you use?
How many host addresses (usable addresses) will be in each subnet?

2^? = 2000 subnets
= 11

borrow 11 
13 host remaining
2^13-2=8190 

---
# Question 
PC1 has an IP address of 10.217.182.223/11.

Identify the following for PC1’s subnet:
1) Network address:
all 0 address after the position

2) Broadcast address:
all 1 address after the position

3) First usable address:
network address + 1

4) Last usable address:
brodcast address -1

5) Number of host (usable) addresses:

---

# VLSM Variable-Length Subnet Masks
Until now, we have practiced subnetting used FLSM (Fixed-Length
Subnet Masks).

This means that all of the subnets use the same prefix length (ie.
subnetting a class C network into 4 subnets using /26).

VLSM (Variable-Length Subnet Masks) is the process of creating
subnets of different sizes, to make your use of network addresses
more efficient.

VLSM is more complicated than FLSM, but it's easy if you follow the
steps correctly.

1) Assign the largest subnet at the start of the address space.
2) Assign the second-largest subnet after it.
3) Repeat the process until all subnets have been assigned.

- adjust from each lan 

![1736994033-vlsm.png](assets/1736994033-vlsm.png)

![1736994101-vlsm2.png](assets/1736994101-vlsm2.png)


- But what prefix length for Toronto lan b
192.198.1.128
/26 => 

2^? => 45
= 6
32 -6 -24 = 2
borrow 2 
/26
![1736995227-.png](assets/1736995227-.png)

Network address: 192.168.1.128/26
Broadcast address: 192.168.1.191/26
First usable address: 192.168.1.129/26
Last usable address: 192.168.1.190/26
Total number of usable host addresses: 62
2^6-2 =62


192.168.1.191 = broadcast address of Toronto LAN B
192.168.1.192 = network address Toronto LAN A (new section)

Network address: 192.168.1.192/27
Broadcast address: 192.168.1.223/27
First usable address: 192.168.1.193/27
Last usable address: 192.168.1.222/27
Total number of usable host addresses: 30


    192.168.1.0/24

192.168.1.223 = broadcast address of Toronto LAN A
192.168.1.224 = network address of Tokyo LAN B

require 8 hosts
❌-> 2^3 = 8
=> 2^4 = 16 ❕
- although /29 allow 8 address 
because still need network and broadcast (extra)


Network address: 192.168.1.224/28
Broadcast address: 192.168.1.239/28
First usable address: 192.168.1.225/28
Last usable address: 192.168.1.238/28
Total number of usable host addresses: 14

Rest -> Point to point connectino only require 2 address

192.168.1.0/24
192.168.1.239 = broadcast address of Tokyo LAN B
192.168.1.240 = network address of point-to-point connection

ccna recommend using /30 instead of/31

Network address: 192.168.1.240/30
Broadcast address: 192.168.1.243/30
First usable address: 192.168.1.241/30
Last usable address: 192.168.1.242/30
Total number of usable host addresses: 2

VLSM => tailed made

http://www.subnettingquestions.com/
https://subnetting.org/
https://subnettingpractice.com/


---

Question:

Question: How many subnets are available with the network 172.16.0.0/26?

To determine how many subnets are available with the network `172.16.0.0/26`, we need to break down the process and calculate the number of subnets that can be created by adjusting the subnet mask.

### Step 1: Understand the `/26` subnet mask
A `/26` subnet mask means that the first 26 bits of the IP address are used for the network portion, leaving 6 bits for the host portion.

- The subnet mask for `/26` in binary looks like this:

  ```
  11111111.11111111.11111111.11000000
  ```

  In decimal, the subnet mask is `255.255.255.192`.

### Step 2: Identify the number of available subnet bits
Since the default subnet mask for a class B address (`172.16.0.0`) is `/16` (which has 16 network bits), moving from `/16` to `/26` means we are borrowing 10 bits from the host portion to create more subnets.

- The formula to calculate the number of subnets is:

  \[
  \text{Number of subnets} = 2^n
  \]

  where `n` is the number of bits borrowed from the host portion. In this case, `n = 26 - 16 = 10`.

### Step 3: Calculate the number of subnets
Now, using the formula, we can calculate the number of subnets:

\[
\text{Number of subnets} = 2^{10} = 1024
\]

### Conclusion:
With the network `172.16.0.0/26`, you can create **1024 subnets**.

- missing lab of subnet

![1737058300-lab1.png](assets/1737058300-lab1.png)
can't be 2^6 because need to -2 

so this should be 2^7 -2

![1737058457-labans1.png](assets/1737058457-labans1.png)
32 -7  = 25
- =/25

ip address 192.168.5.126 255.255.255.128
- + 1 to set up next lan

do show ip g0/1
    - check own ip (as route or gateway)
    - pc2 -> static gateway as bove
    - pc2 -> fastethernet 0  ip 192.168.5.1
    - subnet mask |> 255.255.255.128

- Explain Network Address:

    The IP range for 192.168.5.126 with subnet mask 255.255.255.128 gives a network range from 192.168.5.0 to 192.168.5.127 (network address to broadcast address).

Network and Broadcast Information:
**Network Address: 192.168.5.0**
**Broadcast Address: 192.168.5.127**
This means the usable IP range for devices is 192.168.5.1 to 192.168.5.126.

Lan2 

# Lan1 

![1737059332-lan1.png](assets/1737059332-lan1.png)
int g0/0
ip add **192.168.5.190** **255.255.255.192**
no stut

do sh ip int g0/0
->  result
Internet address is 192.168.5.190/26
Broadcast address is 255.255.255.255

set pc1 gateway => .5.190 (last usable)
set pc1 fastethernet 0 => .5.129(first usable)

## Lan3

![1737059957-lan3.png](assets/1737059957-lan3.png)
 - **frist number = last lan(area) broast ip address 191 + 1** -> network address

- broadcast address: all 1111 after borrow -> 207

- submask net = 11110000 -> 255.240(all borrow become 1)

en 
conf t
int g0/0
ip add 192.168.5.206 255.255.255.240
no stut
this is router

do sh ip int g0/0

pc3  
ip add .5.206
fastethrnet .5.l 193
subnet mask 255.255.255.240

## Lan4

![1737060608-.png](assets/1737060608-.png)


## Point to Point

![1737060901-.png](assets/1737060901-.png)

/30 is safe here

int g0/0/0

## Configure stabic routes on each router so that ol PCs can ping eachother

![1737061112-.png](assets/1737061112-.png)
![1737061174-.png](assets/1737061174-.png)
![1737061188-.png](assets/1737061188-.png)


- Lan  3 to Lan 4:
![1737061262-.png](assets/1737061262-.png)


ping 192.168.5.209 from pc1 to pc4
