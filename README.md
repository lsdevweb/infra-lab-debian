# 🚀 Laboratório de Infraestrutura: Servidor Debian & Docker

Este repositório documenta a implementação de um ambiente cliente-servidor virtualizado, focado em alta disponibilidade, isolamento de serviços e automação.

## 🛠️ Especificações do Ambiente
- **SO Servidor:** Debian 12 (Bookworm)
- **Virtualização:** Hypervisor Tipo 2 (VMware)
- **Orquestração:** Docker & Docker Compose
- **Acesso Remoto:** SSH com autenticação via CLI

## 🏗️ Arquitetura do Projeto
Em vez de uma instalação monolítica, o ambiente utiliza containers para separar as camadas de serviço:

1. **Camada Web:** WordPress sobre servidor Apache.
2. **Camada de Dados:** MySQL 8.0 com volumes persistentes para segurança dos dados.
3. **Rede:** Docker Bridge Network (isolamento do tráfego do banco de dados).

## 💡 Diferenciais Técnicos
- **Infraestrutura como Código (IaC):** Ambiente replicável e versionável através de arquivos YAML.
- **Segurança (Hardening):** Restrição de tráfego de rede interna e gestão de usuários via terminal Linux.
- **Troubleshooting:** Monitoramento de logs em tempo real para validação de conectividade entre containers.

## 🚀 Como subir o ambiente
```bash
# Clonar o repositório
git clone [https://github.com/lsdevweb/infra-lab-debian.git](https://github.com/lsdevweb/infra-lab-debian.git)

# Entrar na pasta
cd infra-lab-debian

# Subir os serviços
docker-compose up -d
## 📊 Status do Laboratório
- **IP Local do Servidor:** 192.168.122.87
- **Porta de Serviço:** 8080
- **Monitoramento:** Logs ativos via `docker logs`
Nota de Segurança: Os endereços de IP e credenciais demonstrados neste laboratório são fictícios ou restritos ao ambiente de rede local isolado, seguindo as boas práticas de segurança da informação.
