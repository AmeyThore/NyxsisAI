# Nyxsis AI 🤖
## @NyxsisAI - https://x.com/Nyxsis_AI
## ✨ Features

- 🛠️ Full-featured Twitter connector for seamless interaction.
- 🔗 Context-aware dialogue generation using the `@ai16z/eliza` framework.
- 👥 Multi-agent support for handling multiple conversations simultaneously.
- 📚 Easily ingest and interact with user-generated content.
- 💾 Retrievable memory for maintaining conversation context.
- 🚀 Highly extensible - create custom actions and responses for your Twitter bot.
- 📦 Just works with minimal setup!

## 🎯 Use Cases

- 🤖 Automated Twitter Chatbot for engaging with users.
- 📈 Business Process Handling through automated responses to inquiries.
- 🕵️ Monitoring and responding to trends and mentions in real-time.
- 🎮 Interactive experiences for users through engaging dialogues.
- 🧠 Gathering user feedback and insights via automated interactions.

## 🚀 Quick Start

### Prerequisites

- [Node.js 23+](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [pnpm](https://pnpm.io/installation)

> **Note for Windows Users:** [WSL 2](https://learn.microsoft.com/en-us/windows/wsl/install-manual) is required.

### Use the Starter (Recommended)

```bash
git clone https://github.com/elizaos/eliza-starter.git
cd eliza-starter
cp .env.example .env
pnpm i && pnpm build && pnpm start
```

Then read the [Documentation](https://elizaos.github.io/eliza/) to learn how to customize your Nyxsis AI.

### Manually Start Nyxsis AI (Only recommended if you know what you are doing)

```bash
# Clone the repository
git clone https://github.com/elizaos/eliza.git

# Checkout the latest release
# This project iterates fast, so we recommend checking out the latest release
git checkout $(git describe --tags --abbrev=0)
```

### Edit the .env file

Copy .env.example to .env and fill in the appropriate values.

```bash
cp .env.example .env
```

Note: .env is optional. If you're planning to run multiple distinct agents, you can pass secrets through the character JSON.

### Automatically Start Nyxsis AI

This will run everything to set up the project and start the bot with the default character.

```bash
sh scripts/start.sh
```

### Edit the character file

1. Open `packages/core/src/defaultCharacter.ts` to modify the default character. Uncomment and edit.

2. To load custom characters:
    - Use `pnpm start --characters="path/to/your/character.json"`
    - Multiple character files can be loaded simultaneously.
3. Connect with Twitter:
    - Change `"clients": []` to `"clients": ["twitter"]` in the character file to connect with Twitter.

### Manually Start Nyxsis AI

```bash
pnpm i
pnpm build
pnpm start

# The project iterates fast, sometimes you need to clean the project if you are coming back to the project
pnpm clean
```

#### Additional Requirements

You may need to install Sharp. If you see an error when starting up, try installing it with the following command:

```bash
pnpm install --include=optional sharp
```
