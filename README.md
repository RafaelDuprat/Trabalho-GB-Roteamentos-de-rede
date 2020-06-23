# Trabalho-GB-Roteamentos-de-rede

TOPOLOGIA DE REDE
![Topologia](https://user-images.githubusercontent.com/67210565/85459884-10751400-b579-11ea-86bb-189d61589f4a.PNG)

CONFIGURAÇÃO DOS ROTEADORES EM SUAS RESPECTIVAS REDES

REDE AS OSPF 100
![AS OSPF 100](https://user-images.githubusercontent.com/67210565/85460218-647ff880-b579-11ea-9f97-c35785dc66ad.PNG)

Primeiramente é necessario clicar no roteador para abri-lo, posteriormente na aba CLI serão setados os comandos abaixo para sua configuração

Router OSPF A
- enable
- configure terminal
- router ospf 1
- network 192.168.10.0 255.255.255.0 area 0
- network 192.168.11.0 255.255.255.0 area 0
- network 192.168.12.0 255.255.255.0 area 0

Router OSPF B
- enable
- configure terminal
- router ospf 1
- network 192.168.12.0 255.255.255.0 area 0
- network 192.168.13.0 255.255.255.0 area 0

Router OSPF C
- enable
- configure terminal
- router ospf 1
- network 192.168.11.0 255.255.255.0 area 0
- network 192.168.14.0 255.255.255.0 area 0

Router OSPF D
- enable
- configure terminal
- router ospf 1
- network 192.168.14.0 255.255.255.0 area 0
- network 192.168.15.0 255.255.255.0 area 0

Router OSPF E
- config terminal
- router ospf 1
- redistribute bgp 100
- network 192.168.13.0 255.255.255.0 area 0
- network 192.168.15.0 255.255.255.0 area 0
- exit

- router bgp 100
- neighbor 192.168.30.2 remote-as 200
- redistribute ospf 1


REDE AS EIGRP 200
![AS EIGRP 200](https://user-images.githubusercontent.com/67210565/85460727-f25be380-b579-11ea-8423-d840cd8bf62a.PNG)

Primeiramente é necessario clicar no roteador para abri-lo, posteriormente na aba CLI serão setados os comandos abaixo para sua configuração

Router EIGRP A
- enable
- config terminal
- router eigrp 200
- network 192.168.20.0
- network 192.168.21.0
- network 192.168.22.0

Router EIGRP B
- enable
- config terminal
- router eigrp 200
- network 192.168.22.0
- network 192.168.23.0

Router EIGRP C
- enable
- config terminal
- router eigrp 200
- network 192.168.21.0
- network 192.168.24.0

Router EIGRP D
- enable
- config terminal
- router eigrp 200
- network 192.168.24.0
- network 192.168.25.0

Router EIGRP E
- enable
- configure terminal
- router eigrp 200
- redistribute bgp 200
- network 192.168.23.0
- network 192.168.25.0
- exit

- router bgp 200
- neighbor 192.168.30.1 remote-as 100
- redistribute eigrp 200



Arquivo .pkt para consulta a topologia configurada
[Trabalho GB Roteamento de redes.zip](https://github.com/RafaelDuprat/Trabalho-GB-Roteamentos-de-rede/files/4821884/Trabalho.GB.Roteamento.de.redes.zip)

