# Xadrez Online

Jogo de xadrez online em um unico arquivo HTML, pronto para publicar no GitHub Pages.

O projeto usa:

- `chess.js` para validar regras reais do xadrez: xeque, xeque-mate, roque, en passant, promocao e empates.
- Firebase Realtime Database para sincronizar a partida entre dois celulares.
- Firebase Authentication anonimo para limitar a sala aos dois jogadores.

## Como publicar no GitHub Pages

1. Abra o repositorio no GitHub.
2. Entre em **Settings > Pages**.
3. Em **Build and deployment**, selecione a branch `main` e a pasta `/root`.
4. Salve e aguarde o GitHub gerar o link.

Depois disso, o jogo ficara disponivel em:

```text
https://SEU-USUARIO.github.io/Xadrez-online/
```

## Como configurar o Firebase

1. Acesse o [Firebase Console](https://console.firebase.google.com/).
2. Crie um projeto.
3. Adicione um app Web.
4. Copie o bloco `firebaseConfig`.
5. Abra o arquivo `index.html`.
6. Substitua o bloco com `COLE_AQUI` pela configuracao real do Firebase.
7. Ative **Authentication > Sign-in method > Anonymous**.
8. Crie um **Realtime Database**.
9. Publique as regras do arquivo `database.rules.json` no Realtime Database.

## Como jogar online

- Um jogador clica em **Criar sala**.
- O jogo gera um codigo e um link.
- O outro jogador abre o link ou digita o codigo.
- Quem cria joga de brancas.
- Quem entra joga de pretas.

## Regras do banco

As regras em `database.rules.json` exigem login anonimo e permitem que apenas os jogadores da sala atualizem a partida.

Elas nao substituem um servidor proprio para partidas publicas ou competitivas, mas sao suficientes para um jogo privado por link.

## Arquivos

- `index.html`: jogo completo.
- `database.rules.json`: regras recomendadas para o Firebase Realtime Database.
