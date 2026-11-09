# Enxoval do Bebê

App web (PWA) para organizar o enxoval do bebê: listas por categoria, progresso por fase
(Fase 1 = essenciais para o parto, Fase 2 = enxoval completo), mala da maternidade,
links salvos, lista para o chá de bebê e plano por semana de gestação.

Tudo fica salvo no próprio celular (localStorage). Use **Você → Exportar/Importar backup**
para guardar uma cópia ou passar os dados para outro aparelho.

## Como usar no iPhone

1. Publique o site (veja abaixo) e abra o endereço no **Safari**.
2. Toque em **Compartilhar → Adicionar à Tela de Início**.
3. O app abre em tela cheia, como um aplicativo, e funciona offline.

## Publicação (GitHub Pages)

O workflow `.github/workflows/pages.yml` publica o site a cada push na branch `main`.
Ative uma vez em **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Arquivos

- `index.html` — o app inteiro (layout, listas de itens e lógica)
- `manifest.webmanifest`, `sw.js`, `icons/` — instalação na tela inicial e uso offline

Para alterar as listas padrão, edite a constante `LISTS` (e `MALA`) em `index.html`.
