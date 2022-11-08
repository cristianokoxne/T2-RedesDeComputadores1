# Trabalho 2: Integração de habilidades - 2022/2
**Disciplina: Redes de Computadores**

**Curso: Engenharia de Computação / Elétrica**

**Nome/RA: Cristiano Koxne  1920251**


## Tarefa 1:  Sub-Redes
| Sub- Rede |             IPv6 - Sub-Rede            |  IPv4 - Sub-Rede  |  IPv4 - Máscara   | IPv4 - Broadcast  |    
|:---------:|:--------------------------------------:|:-----------------:|:-----------------:|:-----------------:|
| Matriz    | 2001:DB8:ACAD:33 *00* ::/64 | 200.200.51.0   | 255.255.255.192 | 200.200.51.63  |
| Filial 1  | 2001:DB8:ACAD:33 *01* ::/64 | 200.200.51.64  | 255.255.255.224 | 200.200.51.95  |
| Filial 2  | 2001:DB8:ACAD:33 *02* ::/64 | 200.200.51.96  | 255.255.255.224 | 200.200.51.127 |
| Filial 3  | 2001:DB8:ACAD:33 *03* ::/64 | 200.200.51.128 | 255.255.255.224 | 200.200.51.159 |
| Filial 4  | 2001:DB8:ACAD:33 *04* ::/64 | 200.200.51.160 | 255.255.255.224 | 200.200.51.192 |
| Filial 5  | 2001:DB8:ACAD:33 *05* ::/64 | 200.200.51.192 | 255.255.255.224 | 200.200.51.223 |
| pb-vit    | 2001:DB8:ACAD:33FF:: *00* :0/112 | 200.200.51.224 | 255.255.255.252 | 200.200.51.227 |
| vit-fb    | 2001:DB8:ACAD:33FF:: *01* :0/112 | 200.200.51.228 | 255.255.255.252 | 200.200.51.231 |
| fb-ita    | 2001:DB8:ACAD:33FF:: *02* :0/112 | 200.200.51.232 | 255.255.255.252 | 200.200.51.235 |
| ita-pb    | 2001:DB8:ACAD:33FF:: *03* :0/112 | 200.200.51.236 | 255.255.255.252 | 200.200.51.239 |
| cv-ita    | 2001:DB8:ACAD:33FF:: *04* :0/112  | 200.200.51.240 | 255.255.255.252 | 200.200.51.243 |



## Tarefa 2: Endereçamento de Dispositivos
| Dispositivo           | Interface | IPv4 | IPv4 - Máscara | IPv4 - Gateway | IPv6/Prefixo | IPv6 - Gateway |
|-----------------------|-----------|------|----------------|----------------|--------------|----------------|
| PC1 | NIC    |  200.200.51.3   |    255.255.255.192       |      200.200.51.1       |       2001:DB8:ACAD:3300::3/64       |       2001:DB8:ACAD:3300::1          |
| PC2 | NIC    |  200.200.51.4    |     255.255.255.192     |      200.200.51.1       |      2001:DB8:ACAD:3300::4/64        |       2001:DB8:ACAD:3300::1          |
| PC3 | NIC    |   200.200.51.67   |     255.255.255.224      |       200.200.51.65      |      2001:DB8:ACAD:3301::3/64        |       2001:DB8:ACAD:3301::1         |
| PC4 | NIC    |   200.200.51.68   |     255.255.255.224      |      200.200.51.65       |      2001:DB8:ACAD:3301::4/64        |        2001:DB8:ACAD:3301::1        |
| PC5 | NIC    |   200.200.51.99   |    255.255.255.224       |       200.200.51.97      |       2001:DB8:ACAD:3302::3/64       |       2001:DB8:ACAD:3302::1          |
| PC6 | NIC    |   200.200.51.100   |     255.255.255.224        |     200.200.51.97       |     2001:DB8:ACAD:3302::4/64        |       2001:DB8:ACAD:3302::1         |
| Switch-Matriz | SVI    |  200.200.51.2    |     255.255.255.192      |      200.200.51.1          |       x       |        x        |
| Switch-Filial1 | SVI    |   200.200.51.66   |    255.255.255.224      |    200.200.51.65            |      x        |        x        |
| Switch-Filial2 | SVI    |   200.200.51.98   |       255.255.255.224         |   200.200.51.97             |       x       |        x        |
| Roteador-Pato Branco  | Fa0/0 |  200.200.51.1    |        255.255.255.192        |       x         |      2001:DB8:ACAD:3300::1/64        |        x        |
| Roteador-Pato Branco  | Se0/0/0 |   200.200.51.225   |        255.255.255.252        |        x        |       2001:DB8:ACAD:33FF::1/112       |       x         |
| Roteador-Pato Branco  | Se0/0/1 |   200.200.51.238   |        255.255.255.252        |       x         |      2001:DB8:ACAD:33FF::3:2/112        |       x         |
| Roteador-Fco. Beltrão | Fa0/0     |   200.200.51.65   |       255.255.255.224         |       x         |      2001:DB8:ACAD:3301::1/64        |        x        |
| Roteador-Fco. Beltrão | Se0/0/0        |        200.200.51.233        |     255.255.255.252           |      x        |       2001:DB8:ACAD:33FF::2:1/112 | x
| Roteador-Fco. Beltrão | Se0/0/1 |   200.200.51.230   |      255.255.255.252        |       x         |       2001:DB8:ACAD:33FF::1:2/112         |      x
| Roteador-Vitorino     | Se0/0/0 |   200.200.51.229   |       255.255.255.252         |       x         |      2001:DB8:ACAD:33FF::1:1/112        |      x          |
| Roteador-Vitorino     | Se0/0/1 |   200.200.51.226   |        255.255.255.252        |       x         |      2001:DB8:ACAD:33FF::2/112        |        x        |
| Roteador-Itapejara    | Se0/0/0 |  200.200.51.237    |       255.255.255.252         |       x         |       2001:DB8:ACAD:33FF::3:1/112       |        x        |
| Roteador-Itapejara    | Se0/0/1 |   200.200.51.234   |        255.255.255.252        |       x         |      2001:DB8:ACAD:33FF::2:2/112        |        x        |
| Roteador-Itapejara    | Fa0/1   |   200.200.51.241   |       255.255.255.252         |       x         |      2001:DB8:ACAD:33FF::4:1/112        |       x         |
| Roteador-Coronel      | Fa0/0   |   200.200.51.97   |       255.255.255.224         |       x         |      2001:DB8:ACAD:3302::1/64        |       x         |
| Roteador-Coronel      | Fa0/1  |   200.200.51.242   |       255.255.255.252         |       x         |      2001:DB8:ACAD:33FF::4:2/112        |        x        |

## Tarefa 3: Tabela de Roteamento
### Roteador Pato Branco
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.51.64 | 255.255.255.224  | 200.200.51.226 | Se0/0/0 |
| 200.200.51.96 | 255.255.255.224  | 200.200.51.226 | Se0/0/0 |
| 200.200.51.228 | 255.255.255.252 | 200.200.51.226 | Se0/0/0 |
| 200.200.51.232 | 255.255.255.252 | 200.200.51.226 | Se0/0/0 |
| 200.200.51.240 |  255.255.255.252 | 200.200.51.226 | Se0/0/0 |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
| 2001:DB8:ACAD:3301::/64 | 2001:DB8:ACAD:33FF::2 | Se0/0/0 |
| 2001:DB8:ACAD:3302::/64 | 2001:DB8:ACAD:33FF::2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::1:0/112 | 2001:DB8:ACAD:33FF::2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::2:0/112 | 2001:DB8:ACAD:33FF::2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::4:0/112 | 2001:DB8:ACAD:33FF::2 | Se0/0/0 |


### Roteador Francisco Beltrão
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.51.0 | 255.255.255.192 | 200.200.51.234 | Se0/0/0 |
| 200.200.51.96 | 255.255.255.224 | 200.200.51.234 | Se0/0/0 |
| 200.200.51.224 | 255.255.255.252 | 200.200.51.234 | Se0/0/0 |
| 200.200.51.236 | 255.255.255.252 | 200.200.51.234 | Se0/0/0 |
| 200.200.51.240 | 255.255.255.252 | 200.200.51.234 | Se0/0/0 |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
| 2001:DB8:ACAD:3300::/64 | 2001:DB8:ACAD:33FF::2:2 | Se0/0/0 |
| 2001:DB8:ACAD:3302::/64 | 2001:DB8:ACAD:33FF::2:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::/112 | 2001:DB8:ACAD:33FF::2:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::3:0/112 | 2001:DB8:ACAD:33FF::2:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::4:0/112 | 2001:DB8:ACAD:33FF::2:2 | Se0/0/0 |

### Roteador Vitorino
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.51.0 | 255.255.255.192 | 200.200.51.230 | Se0/0/0 |
| 200.200.51.64 | 255.255.255.224 | 200.200.51.230 | Se0/0/0 |
| 200.200.51.96 | 255.255.255.224 | 200.200.51.230 | Se0/0/0 |
| 200.200.51.232 | 255.255.255.252 | 200.200.51.230 | Se0/0/0 |
| 200.200.51.236 | 255.255.255.252 | 200.200.51.230 | Se0/0/0 |
| 200.200.51.240 | 255.255.255.252 | 200.200.51.230 | Se0/0/0 |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
| 2001:DB8:ACAD:3300::/64 | 2001:DB8:ACAD:33FF::1:2 | Se0/0/0 |
| 2001:DB8:ACAD:3301::/64 | 2001:DB8:ACAD:33FF::1:2 | Se0/0/0 |
| 2001:DB8:ACAD:3302::/64 | 2001:DB8:ACAD:33FF::1:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::2:0/112 | 2001:DB8:ACAD:33FF::1:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::3:0/112 | 2001:DB8:ACAD:33FF::1:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::4:0/112 | 2001:DB8:ACAD:33FF::1:2 | Se0/0/0 |

### Roteador Itapejara D'Oeste
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.51.0 | 255.255.255.192 | 200.200.51.238 | Se0/0/0 |
| 200.200.51.64 | 255.255.255.224 | 200.200.51.238 | Se0/0/0 |
| 200.200.51.96 | 255.255.255.224 | 200.200.51.242 | Fa0/1 |
| 200.200.51.224 | 255.255.255.252 | 200.200.51.238 | Se0/0/0 |
| 200.200.51.228 | 255.255.255.252 | 200.200.51.238 | Se0/0/0 |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
| 2001:DB8:ACAD:3300::/64 | 2001:DB8:ACAD:33FF::3:2 | Se0/0/0 |
| 2001:DB8:ACAD:3301::/64 | 2001:DB8:ACAD:33FF::3:2 | Se0/0/0 |
| 2001:DB8:ACAD:3302::/64 | 2001:DB8:ACAD:33FF::4:2 | Fa0/1 |
| 2001:DB8:ACAD:33FF::/112 | 2001:DB8:ACAD:33FF::3:2 | Se0/0/0 |
| 2001:DB8:ACAD:33FF::1:0/112 | 2001:DB8:ACAD:33FF::3:2 | Se0/0/0 |

### Roteador Coronel Vivida
#### IPv4
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.51.0 | 255.255.255.192 | 200.200.51.241 | Fa0/1 |
| 200.200.51.64 | 255.255.255.224 | 200.200.51.241 | Fa0/1 |
| 200.200.51.224 | 255.255.255.252 | 200.200.51.241 | Fa0/1 |
| 200.200.51.228 | 255.255.255.252 | 200.200.51.241 | Fa0/1 |
| 200.200.51.232 | 255.255.255.252 | 200.200.51.241 | Fa0/1 |
| 200.200.51.236 | 255.255.255.252 | 200.200.51.241 | Fa0/1 |
#### IPv6
| Rede de Destino/Prefixo | Next Hop | Interface de Saída |
|-----------------|----------|--------------------|
| 2001:DB8:ACAD:3300::/64 | 2001:DB8:ACAD:33FF::4:1 | Fa0/1 |
| 2001:DB8:ACAD:3301::/64 | 2001:DB8:ACAD:33FF::4:1 | Fa0/1 |
| 2001:DB8:ACAD:33FF::/112 | 2001:DB8:ACAD:33FF::4:1 | Fa0/1 |
| 2001:DB8:ACAD:33FF::1:0/112 | 2001:DB8:ACAD:33FF::4:1 | Fa0/1 |
| 2001:DB8:ACAD:33FF::2:0/112 | 2001:DB8:ACAD:33FF::4:1 | Fa0/1 |
| 2001:DB8:ACAD:33FF::3:0/112 | 2001:DB8:ACAD:33FF::4:1 | Fa0/1 |

## Topologia - Packet Tracer
- [ ] ![Trabalho2-Topologia-NomeAluno](trabalho2-20222-topologia-NomeAluno.pkt)

