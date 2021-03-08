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
| 65006:5XX  | Comunidades de prepend (bulk)                  |
| 65006:501  | Adicionar un AS65006 al AS_PATH                |
| 65006:502  | Adicionar dos AS65006 al AS_PATH               |
| 65006:521  | Adicionar un AS65006 al AS_PATH solo clientes  | 
| 65006:522  | Adicionar dos AS65006 al AS_PATH solo clientes |
| 65006:531  | Adicionar un AS65006 al AS_PATH solo peers     |
| 65006:532  | Adicionar dos AS65006 al AS_PATH solo peers    |
| 65006:6XX  | Comunidades de propagación (bulk)              |
| 65006:600  | No propagar fuera de AS65006                   |
| 65006:602  | No propagar a clientes                         |
| 65006:603  | No propagar a peers                            |
| 65006:666  | Blackhole                                      |
| 65006:6XXX | No propagar a ISO 3166-1                       |
| 65006:6032 | No propagar a clientes en Argentina            |
| 65006:6068 | No propagar a clientes en Bolivia              |
| 65006:6858 | No propagar a clientes en Uruguay              |

## Comunidades RFC8092
| Comunidad       | Descripción                                     |
|-----------------|-------------------------------------------------|
| 65006:501:65003 | Adicionar un AS65006 al AS_PATH hacia Argentina | 
| 65006:502:65003 | Adicionar dos AS65006 al AS_PATH hacia Argentina| 
| 65006:501:65004 | Adicionar un AS65006 al AS_PATH hacia Bolivia   | 
| 65006:502:65004 | Adicionar dos AS65006 al AS_PATH hacia Bolivia  | 
| 65006:501:65007 | Adicionar un AS65006 al AS_PATH hacia Uruguay   | 
| 65006:502:65007 | Adicionar dos AS65006 al AS_PATH hacia Uruguay  | 


## Política de comunidades
Las comunidades recibidas de los clientes son propagadas a peers
y otros clientes sin cambios (propagación transparente de comunidades).

# Direcciones de loopback para pruebas
- 198.18.65.1/32
- 2002:10:198:18:64::1/128

# Política de peering
- **No hacemos peering con personas llamadas Nicolás. No insista.**
- Selectiva, solamente con otros tránsitos, contrato a 10 años.
