# Comunidades BGP de Transit2 - AS65006

## Comunidades de identificación
| Comunidad  | Descripción                                    |
|------------|------------------------------------------------|
| 65006:1    | Prefijos originados en 65006                   |
| 65006:2    | Prefijos de clientes                           |
| 65006:3    | Prefijos de peers                              |

## Comunidades de control
| Comunidad  | Descripción                                    |
|------------|------------------------------------------------|
| 65006:90   | LOCAL_PREF menor a por defecto                 |
| 65006:110  | LOCAL_PREF mayor a por defecto                 |
| 65006:666  | Blackhole (RTBH)                               |
| 65006:1000 | No propagar fuera de AS65006                   |
| 65006:1002 | No propagar a clientes                         |
| 65006:1003 | No propagar a peers                            |
| 65006:1032 | No propagar a clientes en Argentina            |
| 65006:1068 | No propagar a clientes en Bolivia              |
| 65006:1858 | No propagar a clientes en Uruguay              |
| 65006:2001 | Adicionar un AS65006 al AS_PATH (prepend x 1)  |
| 65006:2002 | Adicionar dos AS65006 al AS_PATH (prepend x 2) |

# Direcciones de loopback para pruebas
- 198.18.65.1/32
- 2002:10:198:18:64::1/128

# Política de peering
Selectiva, solamente con otros tránsitos, contrato a 10 años.
**No hacemos peering con personas llamadas Nicolás. No insista.**
