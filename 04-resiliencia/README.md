# Resiliência (você se dobra ou quebra?)

- É um conjunto de estratégias adotadas intencionalmente para a "adaptação" de um sistema quando uma falha ocorre.

- Ter estratégias de resiliência nos possibilita minimizar os riscos de perda de dados e transações importantes para o negócio.

## Health Check

- Sem sinais vitais, não é possível saber a "saúde" de um sistema
- Um sistema que não está saudável possui uma chance de se recuperar caso o tráfego pare de ser direcionado a ele temporariamente.
- health check de qualidade 

## Rate Limiting

- Protege o sistema baseado no que ele foi proejtado para suportar (Teste de carga para descobrir o tráfego suportada)
- Preferência programada por tipo de cliente (Bloquear e liberar apenas as requisições importantes)

## Circuit Breaker

- Protege o sistema fazendo com que as requisições feitas para ele sejam negadas. Ex: 500
- Circuito fechado: requisições chegam normalmente
- Circuito aberto: requisições não chegam ao sistema. erro instantâneo ao cliente
- Meio aberto: permite uma quantidade limitada de requisições par averificação se o sistema tem condições de voltar ao ar integralmente.

## API Gateway

- Garante que requisições "inapropriadas" cheguem até o sistema: Ex: usuário não autenticado
- Implementa políticas de rate limiting, helth check, etc

## Service mesh

- Controla o tráfego de rede
- Evita implementações de proteção pelo próprio sistema
- mTLS

## Comunicação assíncrona

- evita perda de dados
- não há perda de dados no envio de uma transação de o server estiver fora
- servidor pode processar a transação em seu tempo quando estiver online
- entender com profundidade o message broker / sistema de stream

## Garantia de entre com Retry

- linear backoff, ex: reenvia a cada segundo
- exponential backoff, ex: reenvia em 1s, 2s, 4s, 8s....
- exponential backoff - Jitter (algoritmo de ruido), algoritmo que varia o tempo de reenvio para N retentativas

## Garantia de entre com Kafka

Cluster, conjunto de brokers

Cluster (Ack 0 - None) = envia a msg p/ broker e não necessita de confirmação
Cluster (Ack 1 - Leader) = envia a msg e recebe a confirmação do broker principal
Cluster (Arc -1 - All) = envia a msg e recebe a confirmação de todos os brokers

## Situações complexas e decisões de alto nível

- O que acontece se o message broker cair?
- Haverá perda de mensagens?
- Seu sistema ficará fora do ar?
- Como garantir resiliência?