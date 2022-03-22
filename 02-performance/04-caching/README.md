# Caching

## Cache na borda / Edge computing

Não realiza novo processamento se já foi processada antes.

1. cache realizado mais próximo ao usuário
2. evita a requisição chegar até o cloud provider/infra
3. normalmente arquivos estáticos
4. CDN - Content Delivery Network
4.1 Cloudflare workers
4.2 Vercel
4.3 Akamai

## Dados estáticos

CSS, HTML, imagens etc.

## Páginas web

## Funções internas

1. Evita reprocessamento de algoritmos pesados
2. Acess oa obanco de dados

## Objetos

Ex: ORM + Banco de Dados, mapeamento

## Exclusivo vs Compartilhado

### Exclusivo

1. irá funcionar na maquina local, baixa latência
2. duplicado entre os nós
3. problemas relacionados a sessões

### Compartilhado

1. maior latência
2. não há dublicação de cache
3. sessões compartilhadas
4. banco de dados externo para armazenar os caches
4.1 Mysql, Redis, Memcache