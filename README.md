# Red.be

[Trello-bord red.be](https://trello.com/b/6EkYezgq/eindopdracht-project-3-systeembeheer-2015-2016-red-be)

## Subnet tabel

| Subnet Naam  	| Nodige hosts	| grootte subnet | Netwerk-adres | Netmask         | CIDR  | Range                         | Broadcast     |
| :---        	| :---	  		| :---           | :---          | :---            | :---  | :---                          | :---          |
| VLAN 4       	| 125	  		| 126            | 192.168.2.0   | 255.255.255.128 | /25   | 192.168.2.1 - 192.168.2.126   | 192.168.2.127 |
| VLAN 3       	| 28	 		| 30             | 192.168.2.128 | 255.255.255.224 | /27   | 192.168.2.129 - 192.168.2.158 | 192.168.2.159 |
| VLAN 2       	| 14   			| 14             | 192.168.2.160 | 255.255.255.240 | /28   | 192.168.2.161 - 192.168.2.174 | 192.168.2.175 |
| Serieel 1    	| 2   			| 2              | 192.168.2.176 | 255.255.255.252 | /30   | 192.168.2.177 - 192.168.2.178 | 192.168.2.179 |
| Serieel 2    	| 2		   		| 2              | 192.168.2.180 | 255.255.255.252 | /30   | 192.168.2.181 - 192.168.2.182 | 192.168.2.183 |

Summarized route van vlan 2, 3 en 4 is: 192.168.2.0/24

## Adrestabel
Bij verbindingen naar een router, of als er naar nergens verwezen wordt, wijst de interface op de interface van de Host.<br>
Bij verbindingen naar een switch, wijst de interface op de interface van de switch.

| Host        	|  Iface	| VLAN  | IP-adres        | Netmask         | Default GW      | Opm.       | Verantw.         |
| :---        	| :---   	| :---: | :---            | :---            | :---            | :---       | :---             |
| Router0     	|   Fa0/0  	|       |                 |                 |                 |            | Abdülkadir Akbel |
|             	|R1 S0/1/0 	|       | 192.168.1.177   |255.255.255.252	 |                 |            | Abdülkadir Akbel |
|          		|R2 S0/0/0 	|       | 192.168.2.177   | 255.255.255.252 |                 |            | Abdülkadir Akbel |
| Router1     	|R0 S0/0/0 	|       | 192.168.1.178 | 255.255.255.252	|                 |            |                  |
|             	|R2 S0/1/0 	|       | 192.168.2.182   | 255.255.255.252 |                 |            |                  |
| Router2     	|R0 S0/0/0 	|       | 192.168.2.178   | 255.255.255.252 |                 |            | Abdülkadir Akbel |
|             	|R1 S0/1/0 	|       | 192.168.2.181   | 255.255.255.252 |                 |            | Abdülkadir Akbel |
|             	|   Fa0/0  	|       | 192.168.2.161   | 255.255.255.240 |                 |            | Abdülkadir Akbel |
|             	|   Fa0/1.3	|       | 192.168.2.129   | 255.255.255.224 |                 | Inter Vlan | Abdülkadir Akbel |
|             	|   Fa0/1.4	|       | 192.168.2.1     | 255.255.255.128 |                 | Inter Vlan | Abdülkadir Akbel |
| Switch1       |   Gig 1/0/1  	|       | 192.168.2.158   | 255.255.255.224 |                 |            |                  |
| Switch3       |   Fa0/1  	|  2    | 192.168.2.174   |255.255.255.240  | 192.168.2.161   | Publieke servers| Bardia S, Leander V|
|             	|        	  |       |                 |                 |                 |            |                  |
| alpha       	|S3 Fa0/2  	|  2    | 192.168.2.162   | 255.255.255.240 | 192.168.2.161   |            |                  |
| charlie     	|S3 Fa0/3  	|  2    | 192.168.2.163   | 255.255.255.240 | 192.168.2.161   |            | Math VR, Jens DV |
| delta       	|S3 Fa0/4  	|  2    | 192.168.2.164   | 255.255.255.240 | 192.168.2.161   |            | Math VR, Jens DV |
| echo        	|S1 Fa0/2  	|  3    | 192.168.2.130   | 255.255.255.224 | 192.168.2.129   |            | Lean Vv, Bard Sh |
| foxtrot     	|S3 Fa0/5  	|  2    | 192.168.2.165   | 255.255.255.240 | 192.168.2.161   |            | Séba Pa,         |
| golf        	|S1 Fa0/3  	|  3    | 192.168.2.131   | 255.255.255.224 | 192.168.2.129   |            | Lean Vv, Bard Sh |
| hotel       	|S1 Fa0/4  	|  3    | 192.168.2.132   | 255.255.255.224 | 192.168.2.129   |            |                  |
| india       	|S1 Fa0/5  	|  3    | 192.168.2.133   | 255.255.255.224 | 192.168.2.129   |            |                  |
| werkstation 3	|S1 Fa0/6  	|  4    | 192.168.2.2     | 255.255.255.128 | 192.168.2.1     |            | Nico Sa, Andy Ne |
| werkstation 4	|S1 Fa0/7  	|  4    | 192.168.2.3     | 255.255.255.128 | 192.168.2.1     |            | Nico Sa, Andy Ne |



# Green.org

[Trello-bord green.org](https://trello.com/b/Yq4CLQPi/eindopdracht-project-3-systeembeheer-2015-2016-green-org)
[Gdocs spreadsheet](https://docs.google.com/spreadsheets/d/1bcAYdEpwB2p638AEfMR7duzDL80iURbCCfKQXmSyZgw/edit?pref=2&pli=1#gid=47640651)

## Subnets

| Subnet    | Clients           | Netwerkadres  | CIDR  | Netmask         | Eerste host   | Laatste host  | Broadcast     |
| :---      | :---   	          | :---          | :---  |  :---           | :---          | :---          | :---          |
| VLAN 4    | private hosts     | 192.168.1.0   | /25   | 255.255.255.128 | 192.168.1.1   | 192.168.1.126 | 192.168.1.127 |
| VLAN 3    | private servers   | 192.168.1.128 | /27   | 255.255.255.224 | 192.168.1.129 | 192.168.1.158 | 192.168.1.159 |
| VLAN 2    | publieke servers  | 192.168.1.160 | /28   | 255.255.255.240 | 192.168.1.161 | 192.168.1.174 | 192.168.1.175 |
| Serial 1  | router 1-router 0 | 192.168.1.176 | /30   | 255.255.255.252 | 192.168.1.177 | 192.168.1.178 | 192.168.1.179 |


## Adrestabel

| Host        | Iface         | VLAN  | IP-adres       | Netmask         | Default GW     | Opm. | Verantwoordelijke(n)   |
| :---        | :---          | :---: | :---           | :---            | :---           | :--- |:---                    |
| Router0     |   Fa0/0       |       |                |                 |                |      |                        |
|             | toR1 S0/1/0   |       | 192.168.1.177  | 255.255.255.252 |                |      |                        |
| Router1     | toR0 S0/0/0   |       | 192.168.1.178  | 255.255.255.252 |                |      |                        |
|             | toR2 S0/1/0   |       | 192.168.2.182  | 255.255.255.252 |                |      |                        |
|             | toS2 Fa0/0.2  | 2     | 192.168.1.161  | 255.255.255.240 |                |      |                        |
|             | toS0 Fa0/1.3  | 3     | 192.168.1.129  | 255.255.255.224 |                |      |                        |
|             | toS0 Fa0/1.4  | 4     | 192.168.1.1    | 255.255.255.128 |                |      |                        |
| Switch0     | VLAN3         |       | 192.168.1.158  | 255.255.255.224 | 192.168.1.129  |      |                        |
| Switch0     | VLAN4         |       | 192.168.1.126  | 255.255.255.128 | 192.168.1.1    |      |                        |
| Switch2     | VLAN2         |       | 192.168.1.174  | 255.255.255.240 | 192.168.1.161  |      |                        |
|             |               |       |                |                 |                |      |                        |
| alpha       | NIC           |   2   | 192.168.1.162  | 255.255.255.240 | 192.168.1.161  | pub  |                        |
| bravo       | NIC           |   2   | 192.168.1.163  | 255.255.255.240 | 192.168.1.161  | pub  |                        |
| charlie     | NIC           |   2   | 192.168.1.164  | 255.255.255.240 | 192.168.1.161  | pub  |                        |
| delta       | NIC           |   2   | 192.168.1.165  | 255.255.255.240 | 192.168.1.161  | pub  |                        |
| echo        | NIC           |   3   | 192.168.1.130  | 255.255.255.224 | 192.168.1.129  | priv |                        |
| foxtrot     | NIC           |   2   | 192.168.1.166  | 255.255.255.240 | 192.168.1.161  | pub  |                        |
| golf        | NIC           |   3   | 192.168.1.131  | 255.255.255.224 | 192.168.1.129  | priv |Jonas V, Jens B         |
| hotel       | NIC           |   3   | 192.168.1.132  | 255.255.255.224 | 192.168.1.129  | priv |                        |
| india       | NIC           |   3   | 192.168.1.133  | 255.255.255.224 | 192.168.1.129  | priv |                        |
| werkstation | NIC           |   4   |  DHCP          |                 |                | priv |                        |
