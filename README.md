# Enxoval do Bebê

App web (PWA) para organizar o enxoval do bebê: listas por categoria, progresso por fase
(Fase 1 = essenciais para o parto, Fase 2 = enxoval completo), mala da maternidade,
links salvos, lista para o chá de bebê e plano por semana de gestação.

Tudo fica salvo no próprio celular (localStorage). Use **Você → Exportar/Importar backup**
para guardar uma cópia ou passar os dados para outro aparelho.

## Endereço

https://enxoval-lucas.web.app (Firebase Hosting, projeto `enxoval-lucas`)

## Como usar no iPhone

1. Abra o endereço acima no **Safari**.
2. Toque em **Compartilhar → Adicionar à Tela de Início**.
3. O app abre em tela cheia, como um aplicativo, e funciona offline.

## Publicação

```
firebase deploy --only hosting
```

A configuração está em `firebase.json` e `.firebaserc`.

## Arquivos

- `index.html` — o app inteiro (layout, listas de itens e lógica)
- `manifest.webmanifest`, `sw.js`, `icons/` — instalação na tela inicial e uso offline
- `firebase.json`, `.firebaserc` — configuração do Firebase Hosting

Para alterar as listas padrão, edite a constante `LISTS` (e `MALA`) em `index.html`.
