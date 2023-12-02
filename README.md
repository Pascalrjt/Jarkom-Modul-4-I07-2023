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