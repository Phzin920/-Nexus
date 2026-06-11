# 🤖 Nexus Bot

Um bot de Discord completo e totalmente customizável, focado em **moderação**, **automação de tarefas** e **organização de servidores**.  
Desenvolvido por **Melancholic**, **PHzin** e **Ninja Code**.

---

## 🚀 Tecnologia

- **Linguagem:** Python 3.8+  
- **Biblioteca:** [discord.py](https://github.com/Rapptz/discord.py) **v2.x** (suporte a comandos slash, modais, views persistentes)  
- **Banco de dados:** SQLite (arquivo local `nexus.db`)  
- **Intents:** `members`, `message_content`, `guilds`, `messages`, `moderation` (todas necessárias para o funcionamento completo)

---

## 📌 Principais funcionalidades

### 🛡️ Moderação
- Comandos slash: `/ban`, `/kick`, `/mute`, `/unmute`, `/clear`, `/warn`, `/lock`, `/unlock`, `/slowmode`, `/softban`, `/tempban`, `/nickname`, `/voicekick`
- Sistema de avisos (`/warnings`, `/delwarn`)
- Registro de ações (modlogs) para auditoria

### ⚙️ Administração e Configuração
- Painel de configuração completo acessível via `/config` (apenas administradores)
- **Verificação por código:** painel com imagem personalizada, cargo automático após digitar código
- **Boas‑vindas e despedida:** mensagens em embed ou texto, com imagem e canal configuráveis
- **Auto‑cargos:** criação de painéis com botões que atribuem/removem cargos
- **Logs:** ative eventos como `message_delete`, `message_edit`, `role_create`, etc.
- **Bloqueador de links:** remove automaticamente mensagens com links, exceto para cargos permitidos
- **Modo guarda:** restringe todo o servidor (apenas administradores podem enviar mensagens/criar convites)
- **Sistema de ponto eletrônico:** `/iniciar-ponto`, `/finalizar-ponto`, `/relatorio-ponto`

### 📢 Utilidades
- Envio de DM ou mensagem em canal via comando (`/dm`, `/enviar-mensagem`)
- Criação e edição de embeds personalizadas (`/embed-criar`, `/embed-editar`)
- Informações: `/userinfo`, `/serverinfo`, `/avatar`, `/ping`
- Biografia automática do bot ao mencioná‑lo ou ao receber DM

---

## 🧩 Comandos (Slash Commands)

### 🔧 Configuração
| Comando | Descrição |
|--------|------------|
| `/config` | Abre o painel de configuração do servidor (admin) |
| `/addrolepanel` | Adiciona um cargo a um painel de auto‑cargos |
| `/logsevent` | Ativa/desativa eventos específicos nos logs |

### 🛡️ Moderação
| Comando | Descrição |
|--------|------------|
| `/ban` | Bane um membro |
| `/kick` | Expulsa um membro |
| `/mute` | Silencia um membro (timeout) |
| `/unmute` | Remove o silêncio |
| `/clear` | Apaga mensagens em massa |
| `/warn` | Adiciona um aviso |
| `/warnings` | Lista os avisos de um membro |
| `/delwarn` | Remove um aviso específico |
| `/lock` | Tranca o canal |
| `/unlock` | Destranca o canal |
| `/slowmode` | Define modo lento |
| `/nickname` | Altera apelido de um membro |
| `/voicekick` | Expulsa um membro de um canal de voz |
| `/softban` | Bane e desbane para limpar mensagens |
| `/tempban` | Bane temporariamente (dias) |
| `/banlist` | Lista todos os banidos |

### 🛡️ Modo Guarda
| Comando | Descrição |
|--------|------------|
| `/iniciar-guard` | Ativa o modo guarda (restringe servidor) |
| `/parar-guard` | Desativa o modo guarda |

### ⏱️ Ponto Eletrônico
| Comando | Descrição |
|--------|------------|
| `/iniciar-ponto` | Marca o início do expediente |
| `/finalizar-ponto` | Marca o fim do expediente |
| `/relatorio-ponto` | Exibe relatório dos últimos 30 dias |

### 📢 Mensagens e Embeds
| Comando | Descrição |
|--------|------------|
| `/dm` | Envia uma DM para um usuário |
| `/enviar-mensagem` | Envia uma mensagem simples em um canal |
| `/embed-criar` | Cria uma embed personalizada |
| `/embed-editar` | Edita uma embed existente |

### ℹ️ Informações
| Comando | Descrição |
|--------|------------|
| `/userinfo` | Mostra informações de um membro |
| `/serverinfo` | Mostra informações do servidor |
| `/avatar` | Exibe o avatar de um membro |
| `/ping` | Latência do bot |
| `/ajuda` ou `/comandos` | Mostra a lista completa de comandos |

---

## ⚙️ Instalação e Execução

### 1. Pré‑requisitos
- Python 3.8 ou superior
- `pip` instalado
- Um aplicativo no [Discord Developer Portal](https://discord.com/developers/applications) com:
  - Bot criado
  - **Intents** ativadas: `SERVER MEMBERS`, `MESSAGE CONTENT`, `PRESENCE` (se desejar)
  - Token do bot

### 2. Clone ou baixe os arquivos
Coloque o arquivo `Nexus.py` (e o banco de dados será gerado automaticamente) em uma pasta.

### 3. Instale as dependências
Abra o terminal na pasta do bot e execute:
```bash
pip install discord.py
