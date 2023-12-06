<h1>Praktikum Modul 4 Jaringan Komputer</h1>
<h3>Kelompok I07</h3>

| NAME                          | NRP       |
|-------------------------------|-----------|
|Pascal Roger Junior Tauran     |5025211072 |
|Mochammad Naufal Ihza Syahzada |5025211260 |

## Soal

- Gunakan prefix IP sesuai dengan prefix IP masing-masing. (10.62)
- Terdapat template spreadsheet untuk mempermudah penilaian, gunakan template tersebut untuk melakukan penghitungan subnetting.
- Hasil perhitungan subnetting dan pohon pembagian IP serta file .pkt di submit pada link di atas.
- File yang didemokan adalah file .pkt yang telah disubmi5t

## Tapologi

- VLSM:<br>
![CPTTapology](https://cdn.discordapp.com/attachments/824131614073683968/1180408128387424286/image.png?ex=657d4fbc&is=656adabc&hm=312449ced231e3fd1664405f592e7df9c7acf11185811ea72970cd0ed67a1487&)

## Routing VLSM
![VLSMRouting](https://cdn.discordapp.com/attachments/824131614073683968/1181949016687267901/IMG_0749.png?ex=6582eacd&is=657075cd&hm=2771d1c25aae9b3d64746c78fba9e08c16afe48dbe8070598566b53cdd05a39f&)

## IP VLSM

- Sorted from largest to smallest `Netmask`<br>

|   Subnet  |   Network Host    |   Netmask |   Addresses   |       Network         | 
|-----------|-------------------|-----------|---------------|-----------------------|
|   A1      |       1116        |   /22     |   1024        |       10.62.1.0       |
|   A4      |       1000        |   /22     |   1024        |       10.62.4.0       |
|   A15     |       1000        |   /22     |   1024        |       10.62.8.0       |
|   A16     |       511         |   /23     |   512         |       10.62.12.0      |
|   A20     |       254         |   /24     |   256         |       10.62.14.0      |
|   A21     |       250         |   /24     |   256         |       10.62.15.0      |
|   A9      |       126         |   /25     |   128         |       10.62.16.0      |
|   A17     |       31          |   /26     |   64          |       10.62.16.128    |
|   A3      |       24          |   /27     |   32          |       10.62.16.192    |
|   A10     |       5           |   /29     |   8           |       10.62.16.224    |
|   A2      |       2           |   /30     |   2           |       10.62.16.232    |
|   A5      |       2           |   /30     |   2           |       10.62.16.236    |
|   A6      |       2           |   /30     |   2           |       10.62.16.240    |
|   A7      |       2           |   /30     |   2           |       10.62.16.244    |
|   A8      |       2           |   /30     |   2           |       10.62.15.248    |
|   A11     |       2           |   /30     |   2           |       10.62.15.252    |
|   A12     |       2           |   /30     |   2           |       10.62.17.0      |
|   A13     |       2           |   /30     |   2           |       10.62.17.4      |
|   A14     |       2           |   /30     |   2           |       10.62.17.8      |
|   A18     |       2           |   /30     |   2           |       10.62.17.12     |
|   A19     |       2           |   /30     |   2           |       10.62.17.16     |

## VLSM Tree
```
10.62.0.0/16 (Network Address)
|
|-- A1: 10.62.1.0/22 (Network Host: 1116)
|
|-- A4: 10.62.4.0/22 (Network Host: 1000)
|
|-- A15: 10.62.8.0/22 (Network Host: 1000)
|
|-- A16: 10.62.12.0/23 (Network Host: 511)
|
|-- A20: 10.62.14.0/24 (Network Host: 254)
|
|-- A21: 10.62.15.0/24 (Network Host: 250)
|
|-- A9: 10.62.16.0/25 (Network Host: 126)
|   |
|   |-- A17: 10.62.16.128/26 (Network Host: 31)
|   |   |
|   |   |-- A3: 10.62.16.192/27 (Network Host: 24)
|   |   |   |
|   |   |   |-- A10: 10.62.16.224/29 (Network Host: 5)
|   |   |   |   |
|   |   |   |   |-- A2: 10.62.16.232/30 (Network Host: 2)
|   |   |   |   |-- A5: 10.62.16.236/30 (Network Host: 2)
|   |   |   |   |-- A6: 10.62.16.240/30 (Network Host: 2)
|   |   |   |   |-- A7: 10.62.16.244/30 (Network Host: 2)
|   |   |   |   |-- A8: 10.62.15.248/30 (Network Host: 2)
|   |   |   |   |-- A11: 10.62.15.252/30 (Network Host: 2)
|   |   |   |   |-- A12: 10.62.17.0/30 (Network Host: 2)
|   |   |   |   |-- A13: 10.62.17.4/30 (Network Host: 2)
|   |   |   |   |-- A14: 10.62.17.8/30 (Network Host: 2)
|   |   |   |   |-- A18: 10.62.17.12/30 (Network Host: 2)
|   |   |   |   |-- A19: 10.62.17.16/30 (Network Host: 2)
```

[Jarkom-Modul-4-I07-2023-Revisi-CPT-VLSM](https://youtu.be/VGqcqe8FWxQ)

## Routing CIDR
![CIDRRouting](https://cdn.discordapp.com/attachments/824131614073683968/1181949551121281195/IMG_0750.png?ex=6582eb4c&is=6570764c&hm=871115c66226d3de4ca330efa58f958b20577bae4eb459b28ba47c6998b90adf&)

## IP CIDR

|  Subnet   |    Network ID     |        Netmask         |     Broadcast    |   Jumlah IP   | 
|-----------|-------------------|------------------------|------------------|---------------|
|    A1     |    10.62.64.0     |    255.255.252.0/22    |   10.62.67.255   |      512      |
|    A2     |    10.62.128.0    |    255.255.255.224/27  |   10.62.128.31   |      31       |
|    A3     |    10.62.128.32   |    255.255.255.252/30  |   10.62.128.35   |      2        |
|    A4     |    10.62.128.64   |    255.255.254.0/23    |   10.62.129.255  |      255      |
|    A5     |    10.64.0.0      |    255.255.255.252/30  |   10.64.0.3      |      2        |
|    A6     |    10.64.8.0      |    255.255.255.252/30  |   10.64.8.3      |      2        |
|    A7     |    10.64.4.0      |    255.255.255.0/24    |   10.64.4.255    |      251      |
|    A8     |    10.64.0.4      |    255.255.252.0/22    |   10.64.3.255    |      1001     |
|    A9     |    10.62.8.4      |    255.255.255.248/29  |   10.64.8.7      |      3        |
|    A10    |    10.62.8.8      |    255.255.255.252/30  |   10.64.8.11     |      2        |
|    A11    |    10.62.8.16     |    255.255.255.252/30  |   10.64.8.19     |      2        |
|    A12    |    10.62.16.64    |    255.255.255.252/30  |   10.62.16.67    |      2        |
|    A13    |    10.62.16.4     |    255.255.255.224/27  |   10.62.16.31    |      25       |
|    A14    |    10.62.16.0     |    255.255.255.252/30  |   10.62.16.3     |      2        |
|    A15    |    10.62.8.16     |    255.255.252.0/22    |   10.62.11.255   |      1001     |
|    A16    |    10.62.8.8      |    255.255.255.252/30  |   10.62.8.11     |      2        |
|    A17    |    10.62.8.4      |    255.255.255.248/29  |   10.62.8.7      |      6        |
|    A18    |    10.62.8.0      |    255.255.252.0/30    |   10.62.8.3      |      2        |
|    A19    |    10.62.0.0      |    255.255.248.0/21    |   10.62.7.255    |      1023     |
|    A20    |    10.62.32.0     |    255.255.255.252/30  |   10.62.32.3     |      2        |
|    A21    |    10.62.16.12    |    255.255.255.0/24    |   10.62.16.255   |      127      |

## CIDR Tree

![CIDR-Tree](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/a9a071a3-56fa-42ef-9700-4e8dcaba1eca)

## CIDR Grouping

*the topo has been re-arrange just to make it easier to group*

![A](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/99ece906-bbf0-40f4-a158-0e15fb042e02)

![B](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/638e0222-2791-4717-84e8-91e4bdf634a7)

![C](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/0450e427-794e-4ea9-b492-f72e3f3eb74f)

![D](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/d8392d8a-89b9-4aeb-adbf-0ea81fc81296)

![E](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/e50e0efe-dfa3-47e7-bee7-04b696fdd5cb)

![F](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/d1d07d01-cb58-4272-a38d-272fb8acb299)

![G](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/6d7056e8-7fb6-4067-9c93-5ece04299360)

![H](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/20586d04-a505-4d3f-b99c-14f5bc25e3a8)

![I](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/5d78e327-ba58-4491-937e-5db071458ef4)

![J](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/bbcbf82f-9669-4d5e-addd-3af79ea6f3d7)

![K](https://github.com/Pascalrjt/Jarkom-Modul-4-I07-2023/assets/89951546/e8d9a0ea-57aa-4fe1-8920-4c211a35c8b4)

## CIDR Routing GNS

### Router

Aura

```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
      address 10.62.32.1
      netmask 255.255.255.252

auto eth2
iface eth2 inet static
      address 10.62.16.65
      netmask 255.255.255.252

auto eth3
iface eth3 inet static
      address 10.64.8.17
      netmask 255.255.255.252
```

Frieren

```
auto eth0
iface eth0 inet static
      address 10.62.16.66
      netmask 255.255.255.252
      gateway 10.62.16.65

auto eth1
iface eth1 inet static
      address 10.62.16.5
      netmask 255.255.255.224

auto eth2
iface eth2 inet static
      address 10.62.16.1
      netmask 255.255.255.252
```

Denken

```
auto eth0
iface eth0 inet static
      address 10.62.32.2
      netmask 255.255.255.252
      gateway 10.62.32.1

auto eth1
iface eth1 inet static
      address 10.62.16.129
      netmask 255.255.255.0
```

Flamme

```
auto eth0
iface eth0 inet static
      address 10.62.16.2
      netmask 255.255.255.252
      gateway 10.62.16.1

auto eth1
iface eth1 inet static
      address 10.62.8.1
      netmask 255.255.255.252

auto eth2
iface eth2 inet static
      address 10.62.8.17
      netmask 255.255.252.0

auto eth3
iface eth3 inet static
      address 10.62.8.9
      netmask 255.255.255.252
```

Fern

```
auto eth0
iface eth0 inet static
      address 10.62.8.2
      netmask 255.255.255.252
      gateway 10.62.8.1

auto eth1
iface eth1 inet static
      address 10.62.0.1
      netmask 255.255.248.0
```

Himmel

```
auto eth0
iface eth0 inet static
      address 10.62.8.10
      netmask 255.255.255.252
      gateway 10.62.8.9

auto eth1
iface eth1 inet static
      address 10.62.8.4
      netmask 255.255.255.248
```

Eisen

```
auto eth0
iface eth0 inet static
      address 10.64.8.18
      netmask 255.255.255.252
      gateway 10.64.8.17

auto eth1
iface eth1 inet static
      address 10.64.8.5
      netmask 255.255.255.248

auto eth2
iface eth2 inet static
      address 10.64.8.9
      netmask 255.255.255.252

auto eth3
iface eth3 inet static
      address 10.64.8.1
      netmask 255.255.255.252

auto eth4
iface eth4 inet static
      address 10.64.0.1
      netmask 255.255.255.252
```

Lugner

```
auto eth0
iface eth0 inet static
      address 10.64.8.2
      netmask 255.255.255.252
      gateway 10.64.8.1

auto eth1
iface eth1 inet static
      address 10.64.0.5
      netmask 255.255.252.0

auto eth2
iface eth2 inet static
      address 10.64.4.1
      netmask 255.255.255.0
```

Linie

```
auto eth0
iface eth0 inet static
      address 10.64.0.2
      netmask 255.255.255.252
      gateway 10.64.0.1

auto eth1
iface eth1 inet static
      address 10.62.128.65
      netmask 255.255.254.0

auto eth2
iface eth2 inet static
      address 10.62.128.33
      netmask 255.255.255.252
```

Lawine

```
auto eth0
iface eth0 inet static
      address 10.62.128.34
      netmask 255.255.255.252
      gateway 10.62.128.33

auto eth1
iface eth1 inet static
      address 10.62.128.1
      netmask 255.255.255.224
```

Heiter

```
auto eth0
iface eth0 inet static
      address 10.62.128.2
      netmask 255.255.255.224
      address 10.62.128.1

auto eth1
iface eth1 inet static
      address 10.62.64.1
      netmask 255.255.252.0
```

### Client & Server

Royalcapital

```
auto eth0
iface eth0 inet static
      address 10.62.16.14
      netmask 255.255.255.0
      gateway 10.62.16.13
```

Willeregion

```
auto eth0
iface eth0 inet static
      address 10.62.16.77
      netmask 255.255.255.0
      gateway 10.62.16.13
```

Lakekoridor

```
auto eth0
iface eth0 inet static
      address 10.62.16.6
      netmask 255.255.255.224
      gateway 10.62.16.5
```

Appetitregion

```
auto eth0
iface eth0 inet static
      address 10.62.0.2
      netmask 255.255.248.0
      gateway 10.62.0.1
```

Laubhills

```
auto eth0
iface eth0 inet static
      address 10.62.0.627
      netmask 255.255.248.0
      gateway 10.62.0.1
```

Rohrroad

```
auto eth0
iface eth0 inet static
      address 10.62.8.18
      netmask 255.255.252.0
      gateway 10.62.8.17
```

Schwermountains

```
auto eth0
iface eth0 inet static
      address 10.62.8.10
      netmask 255.255.255.252
      gateway 10.62.8.9
```

Richter

```
auto eth0
iface eth0 inet static
      address 10.62.8.6
      netmask 255.255.255.248
      gateway 10.62.8.5
```

Revolts

```
auto eth0
iface eth0 inet static
      address 10.62.8.7
      netmask 255.255.255.248
      gateway 10.62.8.5
```

Stark

```
auto eth0
iface eth0 inet static
      address 10.62.8.10
      netmask 255.255.255.252
      gateway 10.62.8.9
```

Turkregion

```
auto eth0
iface eth0 inet static
      address 10.64.0.6
      netmask 255.255.252.0
      gateway 10.64.0.5
```

Grobeforest

```
auto eth0
iface eth0 inet static
      address 10.64.4.2
      netmask 255.255.255.0
      gateway 10.64.4.1
```

Granzchannel

```
auto eth0
iface eth0 inet static
      address 10.62.128.66
      netmask 255.255.254.0
      gateway 10.62.128.65
```

Bredregion

```
auto eth0
iface eth0 inet static
      address 10.62.128.2
      netmask 255.255.255.224
      gateway 10.62.128.1
```

Sein

```
auto eth0
iface eth0 inet static
      address 10.62.64.2
      netmask 255.255.252.0
      gateway 10.62.64.1
```

Riegelcanyon

```
auto eth0
iface eth0 inet static
      address 10.62.64.3
      netmask 255.255.252.0
      gateway 10.62.64.1
```
