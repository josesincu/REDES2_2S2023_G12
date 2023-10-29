# PROYECTO 2
## REDES DE COMPUTADORAS 2
## FACULTAD DE INGENIERIA
## CREACION DE VLAN
>sw1> enable
>
>sw1# configure terminal
>
>sw1(config)# vlan [id]
>
>sw1(config-vlan)# name [nombre]
>
>sw1(config-vlan)# exit
>

## ELIMINAR VLAN
>sw1> enable
>
>sw1# configure terminal
>
>sw1(config)# no vlan [id]
>

##  VTP
### MODOS:
*   SERVIDOR.
*   CLIENTE.
*   TRANSPARENTE.
## CREACION DE VTP
>sw1> enable
>
>sw1# configure terminal
>
>sw1(config)# vtp mode [cliente|server|transparent]
>
>sw1(config)# vtp version [1|2]
>
>sw1(config)# vtp domain [domain]
>
>sw1(config)# vtp password [pass]
>
>sw1(config)# exit
>
>sw1# show vtp status

## MODO TRUNCAL
>sw1> enable
>
>sw1# configure terminal
>
>sw1(config)# interface fastethernet [#]/[#]
>
>sw1(config-if)# switchport mode trunk
>
>sw1(config-if)# switchport trunk allowed vlan [all|#]
>
>sw1(config-if)# exit

## MODO ACCESO
>sw1> enable
>
>sw1# configure terminal
>
>sw1(config)# interface fastethernet [#]/[#]
>
>sw1(config-if)# switchport mode access
>
>sw1(config-if)# switchport access vlan [id]
>
>sw1(config-if)# exit

## TOPOLOGIA GENERAL
*   4 SWITCH MULTICAPA 3650-24PS.
*   8 SWITCH MUTICAPA 3560-24PS.
*   4 SWITCH 2960-24TT.
*   4 LAPTOP.
*   4 PC.
*   3 SERVIDORES.
  
![TOPOLOGIA GENERAL](./Imagenes/TOPOLOGIA.png)
## VTP
### MODO SERVIDOR
* MSW11.
  
![MODO SERVIDOR](./Imagenes/VTP_SERVER.png)
### MODO CLIENTE
* MSW1.
* MSW2.
* MSW3.
* MSW4.
* MSW5.
* MSW6.
* MSW7.
* MSW8.
* MSW9.
* MSW10.
* SW0.
* SW1.
* SW2.
* SW3.
  
![MODO CLIENTE](./Imagenes/VTP_CLIENT.png)
### VLANS
* 121 RRHH.
* 122 IT.
* 123 RRHH_2.
* 124 IT_2.
* 100 SERVER_1.
* 200 SERVER_2.
* 10 WEB_SERVER.
  
![VLANS](./Imagenes/VLANS.png)

## MODE TRUNK
### SWITCH CAPA 3
* MSW1.
* MSW2.
* MSW3.
* MSW4.
* MSW5.
* MSW6.
* MSW7.
* MSW8.
* MSW9.
* MSW10.
* MSW11.
### SWITCH CAPA 2
* SW0.
* SW1.
* SW2.
* SW3.
  
![MODE TRUNK](./Imagenes/MSW11_MODE_TRUNK.png)

## MODE ACCESS
### SWITCHES
* MSW11.
* MSW10.
* SW0.
* SW1.
* SW2.
* SW3
  
![MODE ACCESS](./Imagenes/SW0_MODE_ACCESS_121.png)

![MODE ACCES](./Imagenes/SW0_MODE_ACCESS_122.png)

## LACP
### MODE ACTIVE
* MSW3.
* MSW7.
  
![MODE ACTIVE](./Imagenes/MSW3_LACP_MODE_ACTIVE.png)
### MODE PASSIVE
* MSW8.
* MSW9.

![MODE PASSIVE](./Imagenes/MSW8_LACP_MODE_PASSIVE.png)

## VRRP O HSRP
### ACTIVE
* MSW1.
* MSW4.

![VRRP O HSRP ACTIVE](./Imagenes/HSRP_MSW1.png)
  
### STANDBY
* MSW2.
* MSW6.

![VRRP O HSRP STANDBY](./Imagenes/HRSP_MSW2.png)

## EIGRP
### GRUPO 10 VLAN 121-123
* 192.168.121.0
* 192.178.123.0

### GRUPO 20 VLAN 122-124
* 192.168.122.0
* 192.178.124.0

![EIGRP](./Imagenes/EIGRP_VLAN_121_123.png)

## DHCP
### DHCP SERVER
* SERVER1-DHCP1.
* SERVER2-DHCP2.

![DHCP SERVER 1](./Imagenes/DHCP_SEVER1.png)
## WEB SERVER
* SERVER0-WEB

![WEB SERVER](./Imagenes/RESULTADO_WEB_SERVER.png)

## DHCP HELPER
#### VLAN 
* 121.
* 122.
* 123.
* 124.

![DHCP HELPER](./Imagenes/IP_HELPER.png)

## DHCP IP
### 192.168.121.0
* PC0.
* PC1.

### 192.168.122.0
* LAPTOP0.
* LAPTOP1.

### 192.178.123.0
* LAPTOP3.
* PC3.

### 192.178.124.0
* LAPTOP2.
* PC2.

![DHCP IP](./Imagenes/IP_DHCP.png)
