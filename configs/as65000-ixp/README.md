# ¿Para qué sirve este route server?
Este RS facilita el peering entre los participantes del IXP. Con una sola sesión basta para hacer peering
con los participantes del IXP que tengan sesión con el RS.

Para configurar el RS se necesita hacer peering con el AS65000 a las siguientes direcciones:
- IPv4: 192.0.2.254
- IPv6: 2001:cafe::cafe
 
# Comunidades del Route Server del IXP AS65000

| Comunidad     | Descripción               |
|---------------|---------------------------|
| 0:peer-as     | No propagar a peer-as     |
| 0:65000       | No propagar a ningún peer |
| 65000:peer-as | Propagar a peer-as        |

Ejemplos 
- 0:65003 no propaga los prefijos hacia el AS65003
- 0:65000 y 65000:65001 solamente propaga prefijos hacia el AS65001
