# Bolão OAZ — projeto para GitHub Pages + Google Apps Script

Este pacote mantém o projeto completo em uma estrutura compatível com GitHub Pages:

```text
seu-repositorio/
├── docs/                # Front-end publicado pelo GitHub Pages
├── backend/             # Código-fonte do Google Apps Script
│   ├── Code.gs
│   └── appsscript.json
├── .gitignore
└── README.md
```

## Publicar o front-end

1. Envie todos os arquivos deste pacote à raiz do repositório.
2. Em **Settings → Pages**, escolha **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/docs`.
4. Salve.

O GitHub Pages publica somente o conteúdo de `docs/`.

## Backend

O conteúdo de `backend/Code.gs` **não é apagado nem executado pelo GitHub Pages**. Ele deve ser publicado separadamente no Google Apps Script como **Web App**.

A URL do Web App usada pelo site está em `docs/js/config.js`, no campo `apiUrl`.

## Segurança

A planilha-base não foi incluída neste pacote de repositório para evitar exposição em um GitHub público. Mantenha-a no Google Drive/Google Sheets e não a envie ao repositório.
