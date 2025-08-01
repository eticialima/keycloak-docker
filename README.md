# Keycloak com PostgreSQL

Este projeto configura um ambiente Keycloak completo usando Docker Compose com banco de dados PostgreSQL.

## O que faz

- **Keycloak**: Servidor de autenticação e autorização (Identity Provider)
- **PostgreSQL**: Banco de dados para persistir dados do Keycloak
- **Rede isolada**: Comunicação segura entre os serviços

## Como usar

1. **Iniciar os serviços:**
   ```bash
   docker-compose up -d
   ```

2. **Acessar o Keycloak:**
   - URL: http://localhost:8080
   - Admin: `admin`
   - Senha: `admin`

3. **Parar os serviços:**
   ```bash
   docker-compose down
   ```

## Configuração

- **Keycloak**: Porta 8080 (HTTP) e 8443 (HTTPS)
- **PostgreSQL**: Porta 5433 (para evitar conflitos com outras instâncias)
- **Dados**: Persistidos no volume `pgdata`

## Notas

- Configurado em modo desenvolvimento (`start-dev`)
- Health checks e métricas habilitadas
- PostgreSQL usa porta 5433 no host para evitar conflitos
