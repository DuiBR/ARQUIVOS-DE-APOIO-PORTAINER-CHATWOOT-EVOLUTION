# 🐳 Instalação do Docker com Swarm e Portainer

Este guia fornece os passos para configurar rapidamente o Docker com suporte ao **Swarm Mode** e o **Portainer** para gerenciamento visual dos containers.

---

## ⚙️ Preparação do Ambiente

Execute os comandos abaixo para atualizar o sistema e garantir permissões adequadas:

```bash
sudo apt-get update ; apt-get install -y apparmor-utils

Defina o nome do host da máquina:
hostnamectl set-hostname myserver

nano /etc/hosts
