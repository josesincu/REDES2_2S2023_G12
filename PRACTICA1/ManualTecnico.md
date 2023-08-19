# PRACTICA 1
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








