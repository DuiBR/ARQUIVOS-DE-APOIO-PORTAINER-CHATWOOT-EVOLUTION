# 🤖 Instalação Chatwoot e suas Dependencias

Este guia fornece os passos para instalar rapidamente o Chatwoot e suas dependencias.

---

## ⚙️ Preparação do Ambiente

Execute este comando no container do postgres:

```bash
psql -U postgres

create DATABASE chatwoot;
```

## 📟 Comandos úteis para instalar e atualizar o chatwoot:
### 📌 Executar em modo ash ou sh no container app do chatwoot

Comando para instalar o chatwoot:

```bash
bundle exec rails db:chatwoot_prepare
```

Comando para atualizar o chatwoot:

```bash
bundle exec rails db:migrate
```

# 🙌 Apoie este Projeto
Se este conteúdo te ajudou e você quiser apoiar o projeto, você pode enviar um Pix:

## 📲 Chave Pix: rodrigo.tanci@inovanode.com.br

Seu apoio é muito bem-vindo! 💜


