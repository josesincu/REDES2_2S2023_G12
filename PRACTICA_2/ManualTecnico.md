# PRACTICA 2
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

## PORT-SECURITY
>sw1> enable
>
>sw1# configure terminal
>
>sw1(config)# interface fastethernet [#]/[#]
>
>sw1(config-if)# switchport port-security
>
>sw1(config-if)# switchport port-security mac-address ####.####.###
>
>sw1(config-if)# exit

## TOPOLOGIA GENERAL
*   12 SWITCH
*   5 LAPTOP
*   5 DESKTOP
![TOPOLOGIA GENERAL](./Imagenes/TOPOLOGIA_GENERAL.png)


## CONFIGURACION DE IP
### AREA PRIMARIA
#### SE ASIGNARON IPS A LAS MAQUINAS CON DIRECCION DE IP 192.168.13.X
![PRIMARIA PC0](./Imagenes/pc0.png)
![PRIMARIA PC1](./Imagenes/pc1.png)

### AREA BASICO
#### SE ASIGNARON IPS A LAS MAQUINAS CON DIRECCION DE IP 192.168.23.X
![BASICO LAPTOP0](./Imagenes/laptop0.png)
![BASICO PC2](./Imagenes/pc2.png)

### AREA DIVERSIFICADO
#### SE ASIGNARON IPS A LAS MAQUINAS CON DIRECCION DE IP 192.168.33.X
![DIVERSIFICADO LAPTOP1](./Imagenes/laptop1.png)
![DIVERSIFICADO LAPTOP2](./Imagenes/laptop2.png)
![DIVERSIFICADO LAPTOP3](./Imagenes/laptop3.png)
![DIVERSIFICADO LAPTOP4](./Imagenes/laptop4.png)

## CONFIGURACION DEL VTP
### MODO SERVER
![VTP SERVER](./Imagenes/server.png)

### MODO CLIENT
![VTP CLIENT](./Imagenes/client.png)

### CREANDO LAS VLANS EN SWITCH SERVER
![CREANCION VLNAS](./Imagenes/VLAN_SERVER.png)

## MODO TRUNK
### AGREANGO EL MODO TRUNKAL EN LOS SWITCH
![MODO TRUNK](./Imagenes/TRUNK_SW10.png)

## MODO ACCESS
### AGREANGO EL MODO ACCESS PRIMARIA
![ACCESS PRIMARIA](./Imagenes/ACCCESS_SW0.png)

### AGREANGO EL MODO ACCESS BASICO
![ACCESS BASICO](./Imagenes/ACCESS_SW1_BASICO.png)

### AGREANGO EL MODO ACCESS DIVERSIFICADO
![ACCESS DIVERSIFICADO](./Imagenes/ACCESS_SW2_DIVERSIFICADO.png)

## SPANNING-TREE
### SWITCH ROOT
![SWITCH ROOT](./Imagenes/Root_spaning-tree.png)

## RESULTADO CONVERGENCIA PVST Y RAPID PVST
### SPANNING-TREE PVST
#### PRIMARIA
![PVST PRIMARIA](./Imagenes/PVST_PRIMARIA.png)
#### BASICO
![PVST BASICO](./Imagenes/PVST_BASICO.png)
#### DIVERSIFICADO
![PVST DIVERSIFICADO](./Imagenes/PVST_DIVERSIFICADO.png)

### SPANNING-TREE RSTP
#### PRIMARIA
![RSTP PRIMARIA](./Imagenes/RPVST_PRIMARIA.png)
#### BASICO
![RSTP BASICO](./Imagenes/RPVST_BASICO.png)
#### DIVERSIFICADO
![RSTP DIVERSIFICADO](./Imagenes/RPVST_DIVERSIFICADO.png)

|ESCENARIO | PROTOCOLO SPANNING-TREE | RED PRIMARIA |  RED BASICO | RED DIVERSIFICADO |
|:--------:|:-----------------------:|:------------:|:-----------:|:-----------------:|
|   1      |           PVST          |  46 SEGUNDOS | 27 SEGUNDOS |    26 SEGUNDOS    |
|   2      |     RAPID PVST          |  1 SEGUNDOS  |  0 SEGUNDOS |     0 SEGUNDOS    |

#### AL REALIZAR  LAS MEDICIONES CORRESPONDIENTES DE LOS PROTOCOLOS DE SPANNING-TREE
#### SE CONCLUYE QUE EL PROTOCOLO CON MENOR LATENCIA ES EL RAPID SPANNING TREE
#### YA QUE CONVERGE RAPIDAMENTE.

## PORT SECURITY

### CONFIGURACION DE SW2
![PORT SECURITY](./Imagenes/PORT_SECURITY.png)







