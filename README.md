# Discord Moderation Bot

Um bot de moderação robusto e completo desenvolvido em Node.js, focado em gerenciamento de servidores e segurança.

## ✨ Funcionalidades Principais

### 🛡️ Sistema de Moderação
- **Banimento e Expulsão**: Comandos `/ban`, `/unban` e `/kick` com suporte a logs e DMs.
- **Silenciamento (Timeout)**: Sistema de castigo temporário com `/mute` e `/unmute`.
- **Moderação de Voz**: Silencie usuários em chamadas com `/mutecall` e `/unmutecall`.
- **Controle de Chat**:
  - `/clear`: Limpeza de mensagens em massa (com filtro por usuário).
  - `/lock` e `/unlock`: Bloqueie e desbloqueie canais inteiros.
  - `/slowmode`: Defina o modo lento do canal.
- **Gerenciamento de Usuários**:
  - `/nick`: Altera apelidos.
  - `/role`: Adiciona ou remove cargos.

### ⚠️ Sistema de Advertências (Warns)
Um sistema completo de avisos salvo no banco de dados:
- `/warn`: Adverte um usuário.
- `/unwarn`: Remove advertências (pelo ID ou a última).
- `/warnings`: Visualiza o histórico de infrações de um membro.

### 🚫 Sistema de Blacklist
Ferramenta para desenvolvedores bloquearem usuários de utilizarem o bot globalmente.
- `/blacklist add/remove/info`

### 📝 Logs Automatizados
Todo comando de moderação gera um log detalhado em um canal configurável.
- Use `/setlogs` para definir o canal de auditoria.

### 📢 Outros
- `/say`: Envie mensagens através do bot (texto ou embed).

## 🚀 Início Rápido

### 1. Instale as Dependências
```bash
npm install
```

### 2. Configure as Variáveis de Ambiente
Crie um arquivo `.env` na raiz do projeto:
```env
CLIENT_TOKEN=seu_token_do_bot
DATABASE=seu_uri_do_mongodb
```

### 3. Configure o Bot
Edite `src/config/config.json` para definir donos e outras opções.

### 4. Inicie o Bot
```bash
node .
```

## ☁️ Deploy na ShardCloud

Este projeto já vem configurado para a **ShardCloud**:
1. O arquivo `.shardcloud` já está presente.
2. Defina as variáveis de ambiente no painel.
3. Faça o upload e inicie!

## 📋 Estrutura do Projeto

```
moderation-bot/
├── src/
│   ├── assets/            # Ativos estáticos
│   ├── commands/          # Comandos do bot (Slash)
│   ├── config/            # Arquivos de configuração (config.json)
│   ├── events/            # Eventos do Discord
│   ├── functions/         # Funções utilitárias
│   ├── handler/           # Carregadores de comandos, eventos, etc.
│   ├── interactions/      # Interações (Buttons, Selects, Modals)
│   └── structures/        # Classes base (Client, etc.)
├── .env.example           # Exemplo de variáves de ambiente
├── .shardcloud            # Configuração ShardCloud
├── index.js               # Ponto de entrada
└── package.json           # Dependências e scripts
```

## 🛠️ Tecnologias

- **Node.js** & **Discord.js v14**
- **MongoDB** (Mongoose) para persistência de dados (Warns, Logs, Blacklist).

## 📄 Licença

MIT