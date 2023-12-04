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

## Routing CIDR

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
