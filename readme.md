# i9 Fitness — Landing Page

Landing page para a **Academia i9 Fitness** (unidade Cohatrac III, São Luís/MA), construída em **HTML e CSS puro**, sem frameworks e sem JavaScript.

## Sobre o projeto

O objetivo da página é apresentar a academia, seu método de treino, estrutura, planos e localização, com foco em converter visitantes em contato via WhatsApp e Instagram.

**Identidade visual:** paleta escura (tons de concreto/aço) com um vermelho-ember como cor de destaque, tipografia condensada de impacto (Anton) combinada com uma fonte mono (IBM Plex Mono) para dados e rótulos — remetendo a placar/monitor de performance. O elemento de assinatura é uma linha de pulso (batimento) no hero, e os planos são nomeados como anilhas de peso (10KG / 20KG / 30KG), reforçando o universo da academia.

## Estrutura de arquivos

```
.
├── index.html            → todo o markup da página
├── README.md              → este arquivo
└── styles/
    ├── index.css          → arquivo de entrada: só importa os outros dois
    ├── global.css         → tokens (:root), reset, tipografia base, botões, animação de reveal
    └── styles.css         → estilos específicos de cada seção (header, hero, planos, etc.)
```

O `index.html` carrega apenas `styles/index.css`, que por sua vez importa `global.css` e `styles.css` nessa ordem:

```css
/* styles/index.css */
@import url("./styles.css");
@import url("./global.css");
```

**Por que separar assim:**
- `global.css` guarda o que é reaproveitável em qualquer página do site (cores, fontes, reset, botões, animações genéricas) — se um dia crescer para mais páginas, esse arquivo não muda.
- `styles.css` guarda o que é específico *desta* landing page (seções: hero, planos, depoimentos, localização etc.).
- `index.css` é só o "índice" que junta os dois, então o HTML precisa referenciar um único `<link>`.

## Seções da página

| Seção | Conteúdo |
|---|---|
| Ticker bar | Horário de funcionamento, endereço e aviso de Gympass em loop |
| Header | Logo, navegação por âncoras e botão de WhatsApp |
| Hero | Chamada principal + CTA de aula experimental + linha de pulso animada |
| Stats | Números rápidos (horário, dias abertos, unidades, seguidores) |
| Método | Explicação da abordagem de treino em 4 passos |
| Estrutura | Cards com modalidades e diferenciais (musculação, funcional, Gympass etc.) |
| Planos | Mensal / Trimestral / Anual, com CTA para consultar valor no WhatsApp |
| Depoimentos | Avaliações resumidas com base em reviews públicas |
| Localização | Endereço, horário, contato e mapa incorporado do Google Maps |
| CTA final | Última chamada para agendar aula experimental |
| Footer | Links de contato e redes sociais |

## Dados reais usados

- **Endereço:** Rua Seis, 2 — Cohatrac III, São Luís/MA, 65054-560
- **Horário:** Segunda a sexta, 06h–22h · Sábado, 08h–12h
- **Telefone/WhatsApp:** (98) 98554-6423
- **Instagram:** [@academiai9cohatrac](https://www.instagram.com/academiai9cohatrac/)

Preços dos planos **não** foram incluídos por não termos essa informação confirmada — os botões direcionam para o WhatsApp para consulta de valores.

## Como usar

1. Baixe os 4 arquivos mantendo a mesma estrutura de pastas (a pasta `styles/` precisa ficar no mesmo nível do `index.html`).
2. Abra o `index.html` direto no navegador — não precisa de servidor local nem instalação.
3. Para editar conteúdo (textos, links, endereço), mexa no `index.html`.
4. Para editar cores, fontes ou espaçamentos globais, mexa no `global.css`. Para ajustar uma seção específica (ex: o grid de planos), mexa no `styles.css`.

## Compatibilidade

Sem JavaScript. As animações de entrada das seções usam `animation-timeline: view()` (CSS puro), com fallback via `@supports` para navegadores que ainda não suportam essa propriedade — o conteúdo aparece normalmente de qualquer forma. Layout responsivo com breakpoints em `920px` e `720px`.

## Observação importante

Antes de publicar a página oficialmente, vale confirmar se a documentação da unidade (registro no CREF, alvará sanitário e certificado do Corpo de Bombeiros) está regularizada, já que houve uma interdição reportada pela fiscalização do CREF21/MA e Procon/MA em janeiro de 2026.


<img src="/styles/style/assets/i9-fitness-1080x1080.png" alt="#">