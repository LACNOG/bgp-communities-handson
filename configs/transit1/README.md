# TRANSIT1

![TRANSIT1](/assets/img/lacnog-handson-bgp-as65005.png)

*TRANSIT1* es un proveedor de servicios que interconecta clientes en varias regiones.

Aprende y publica prefijos IP propios desde el AS65005, también brinda servicios de tránsito IPv4/IPv6 entre sus clientes (AS65007, AS65001 y AS65002).  

*TRANSIT1* se interconecta al IXP en donde mantiene peerings BGP contra el route-server y con su querido vecino *TRANSIT2*

## Tablas de comunidades

![Tablas de comunidades del AS65005](/assets/img/lacnog-handson-bgp-communities-as65005.png)


## Direcciones de Loopback para pruebas

* 198.18.6.66
* 2002::2002

## Política de Peering

En *TRANSIT1* la política de peering es selectiva. No confiamos en sistemas autónomos intergalácticos. **No insista**

## Información extra

El equipo emulado es un router Cisco que corre IOS-XR. Para entender más acerca de la configuración de políticas de ruteo en esta plataforma, por favor referirse a: 
[Route Policy Language en Cisco IOS XR](https://www.cisco.com/c/dam/en_us/training-events/le31/le46/cln/pdf/webinar_slides/RPL-Webinar-Slides-CLN.pdf)