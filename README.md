# Mundial 2026 Hub

Prototipo navegavel de um website para acompanhar o Mundial 2026 com:

- resultados e estados de jogo;
- estatisticas aprofundadas;
- previsoes antes dos jogos;
- comparacao entre previsao e resultado final;
- informacao sobre selecoes, jogadores, curiosidades e estadios;
- bloco de arquitetura para ligar APIs reais.

## Publicar com GitHub + Vercel

1. No Vercel, cria um novo projeto a partir deste repositorio.
2. Em Project Settings > Environment Variables, adiciona:
   - `API_FOOTBALL_KEY`: a tua chave da API-Football;
   - `API_FOOTBALL_LEAGUE_ID`: `1`;
   - `API_FOOTBALL_SEASON`: `2026`.
3. Faz deploy.

Nao coloques a API key no `data.js`, no `app.js`, no GitHub ou no chat. A key deve ficar apenas nas variaveis de ambiente do Vercel.

## Dados reais

A camada atual usa `data.js` como fallback local. Em producao, o frontend tenta carregar `/api/football`, que chama a API-Football a partir de uma funcao serverless no Vercel.
