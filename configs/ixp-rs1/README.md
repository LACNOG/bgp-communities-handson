# Comunidades del Route Server del IXP AS65000

| Comunidad     | Descripción               |
|---------------|---------------------------|
| 0:peer-as     | No propagar a peer-as     |
| 0:65000       | No propagar a ningún peer |
| 65000:peer-as | Propagar a peer-as        |

Ejemplos 
- 0:65003 no propaga los prefijos hacia el AS65003
- 0:65000 y 65000:65001 solamente propaga prefijos hacia el AS65001
