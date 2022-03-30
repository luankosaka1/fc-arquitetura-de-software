# Escalabilidade

É a capacidade de sistemas suportarem o aumento dos workloads incrementando o custo em menor ou igual proporção

## Escalabilidade vs Performance

### Performance

Foco em reduzir a latência ed aumentar o throughput. Ex: escala vertical

### Escalabilidade

Visa termos a possibilidade de aumentar ou diminuir o throughput add ou removendo a capacidade computacional. Ex: escala horizontal, necessário proxy reverso

## Escala Vertical

### Escalando software - Descentralização

1. Disco efêmero
2. Servidor de aplicação vs Servidor de assets
3. Cache centralizado
4. Sessões Centralizadas
5. Upload/Gravação de arququos

## Banco de Dados

1. Aumentando recursos computacionais (limitado)
2. Distribuindo responsabilidades (escrita vs leitura)
3. Shards de forma horizontal
4. Serverless

### Otimização de queries e índices

1. Trabalhe com índices de forma consciente
2. APM (Application performance monitoring) nas queries
3. Explain na queries
4. CQRS (Command Query Responsibility Segregation)

## Proxy Reverso

É um servidor que fica na frente dos servidores web e encaminha as solicitações do cliente para esses servidores web.

### Soluções populares de proxy reverso

1. Nginx
2. HAProxy (HA = High Availability)
3. Traefik