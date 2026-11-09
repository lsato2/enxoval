# Enxoval do Bebê

App web (PWA) para organizar o enxoval do bebê: listas por categoria, progresso por fase
(Fase 1 = essenciais para o parto, Fase 2 = enxoval completo), mala da maternidade,
links salvos, lista para o chá de bebê e plano por semana de gestação.

Login com e-mail e senha (Firebase Authentication). O enxoval fica no Firestore e é
compartilhado em tempo real entre os membros: em **Você → Compartilhar o enxoval**, convide
pela conta de e-mail; a pessoa cria a conta com esse e-mail e entra direto no mesmo enxoval.

## Endereço

https://enxoval-lucas.web.app (Firebase Hosting, projeto `enxoval-lucas`)

## Como usar no iPhone

1. Abra o endereço acima no **Safari**.
2. Toque em **Compartilhar → Adicionar à Tela de Início**.
3. O app abre em tela cheia, como um aplicativo, e funciona offline.

## Publicação

```
firebase deploy --only hosting,firestore
```

A configuração está em `firebase.json` e `.firebaserc`; as regras de acesso em `firestore.rules`.
O SDK do Firebase (10.12.2) fica em `vendor/firebase/`, copiado do pacote npm oficial.

## Arquivos

- `index.html` — o app inteiro (layout, listas de itens e lógica)
- `manifest.webmanifest`, `sw.js`, `icons/` — instalação na tela inicial e uso offline
- `firebase.json`, `.firebaserc` — configuração do Firebase Hosting

Para alterar as listas padrão, edite a constante `LISTS` (e `MALA`) em `index.html`.
