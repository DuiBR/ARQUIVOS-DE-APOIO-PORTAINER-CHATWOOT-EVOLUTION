# 🐳 Instalação do Docker com Swarm e Portainer

Este guia fornece os passos para configurar rapidamente o Docker com suporte ao **Swarm Mode** e o **Portainer** para gerenciamento visual dos containers.

---

## ⚙️ Preparação do Ambiente

Execute os comandos abaixo para atualizar o sistema e garantir permissões adequadas:

```bash
sudo apt-get update ; apt-get install -y apparmor-utils
```

Defina o nome do host da máquina:

```bash
hostnamectl set-hostname myserver
```

Edite o arquivo de hosts para refletir o novo hostname:

```bash
nano /etc/hosts
```

Altere a linha:

```bash
127.0.0.1 localhost
```

Para:

```bash
127.0.0.1 myserver
```

## 🐋 Instalando o Docker

Execute o script oficial para instalação automática do Docker:

```bash
curl -fsSL https://get.docker.com | bash
```

Inicialize o modo Swarm:

```bash
docker swarm init
```

Crie a rede overlay para os serviços:

```bash
docker network create --driver=overlay swarm_network
```

## 🚦 Configurando o Traefik

Crie o arquivo de configuração do Traefik:

```bash
nano traefik.yaml
```

Depois, faça o deploy do stack:

```bash
docker stack deploy --prune --resolve-image always -c traefik.yaml traefik
```

## 📊 Instalando o Portainer

Crie o arquivo de configuração do Portainer:

```bash
nano portainer.yaml
```

Depois, faça o deploy do stack:

```bash
docker stack deploy --prune --resolve-image always -c portainer.yaml portainer
```

# 🙌 Apoie este Projeto
Se este conteúdo te ajudou e você quiser apoiar o projeto, você pode enviar um Pix:

##📲 Chave Pix: rodrigo.tanci@inovanode.com.br

Seu apoio é muito bem-vindo! 💜


