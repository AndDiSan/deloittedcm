# Vue 3 DevContainer Template

Template per progetti Vue 3 con DevContainer configurato per pnpm e Vuetify.

## Prerequisiti

- Docker Desktop
- Visual Studio Code
- VS Code Remote Development Extension Pack

## Come usare questo template

### Creare un nuovo progetto

1. Clicca il pulsante "Use this template" su GitHub
2. Scegli un nome per il nuovo repository
3. Clona il nuovo repository:

```bash
git clone https://github.com/TUO-USERNAME/NUOVO-REPO-NAME.git
cd NUOVO-REPO-NAME  
```

4. Apri in VS Code e avvia il DevContainer:

   - VS Code chiederà di riaprire in container
   - O usa Command Palette (F1): "Reopen in Container"

5. Una volta nel container, crea la tua app Vue:

```bash
pnpm create vuetify
```

6. Segui le istruzioni di setup di Vuetify

### Struttura del progetto

```
.
├── .devcontainer/
│   ├── devcontainer.json
│   └── Dockerfile
├── .gitignore
└── README.md
```

## Caratteristiche

- Node 20
- pnpm preconfigurato
- Vuetify supporto
- Firebase Tools
- Git integrato
- Volume Docker per workspace
- VS Code extensions preconfigurate

## Utilizzo su altre macchine

1. Clona il repository:

```bash
git clone https://github.com/AndDiSan/nome-progetto.git
cd nome-progetto
```

2. Apri in VS Code e avvia il DevContainer:

   - Il container si costruirà automaticamente
   - Tutte le dipendenze saranno installate
   - L'ambiente sarà identico su ogni macchina

3. Avvia il progetto:

```bash
pnpm install  # se necessario
pnpm dev
```

## Contributing

Per contribuire al progetto:

1. Fai un fork del repository

2. Crea un nuovo branch per le tue modifiche
3. Fai commit delle tue modifiche
4. Crea una Pull Request

## Manutenzione

Ultimo aggiornamento: 2024-02-02 10:53:24 UTC  
Mantenuto da: [@AndDiSan](https://github.com/AndDiSan)

## Licenza

[MIT License](LICENSE)
