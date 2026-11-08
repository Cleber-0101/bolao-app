# ⚽ Bolão App

Site de bolão para um jogo da Copa do Mundo, criado e **usado de verdade** pelos colegas da empresa onde eu trabalhava: cada pessoa faz o palpite, o resultado é lançado e o ranking é calculado sozinho.

## Stack
HTML · CSS · JavaScript · Google Apps Script (back-end serverless) · Google Sheets (dados) · GitHub Pages (deploy)

## Arquitetura
```
docs/      -> front-end (palpite, resultado, ranking) publicado no GitHub Pages
backend/   -> Code.gs, publicado como Web App no Google Apps Script
```
O front chama o Web App (URL em `docs/js/config.js`), que lê e grava os palpites numa planilha. A planilha fica fora do repositório. As regras de pontuação estão em [`REGRAS_DE_PONTUACAO.txt`](REGRAS_DE_PONTUACAO.txt).
