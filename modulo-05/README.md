# Networks
Gerenciar conexões do docker com outras plataformas ou outros containers.

Existem três tipos de drivers de rede:
- bridge (default): conexão entre containers
- overlay: conecta multiplas instâncias do docker e habilita o uso do swarm
- ipvlan: conexão por IP
- host: conexão com o host do docker
- macvlan: conexão por mac address
- none: nenhuma conexão
- plugins: extensões de parceiros

## Tipos de conexão
Os containers costumam ter três tipos de conexão:
- externa
- com o host
- entre containers  