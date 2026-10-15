# Vinheria Agnello

Site institucional simples para o Check-Point de Front-End Design, baseado no caso da Vinheria Agnello.

## Descrição do caso

Vinheria familiar em São Paulo há mais de 15 anos, dirigida por Giulio e sua filha Bianca. Diferencial é o atendimento consultivo sobre uva, região, rótulo e harmonização. Com a pandemia, o movimento da loja física caiu e a empresa busca um portal digital que reproduza a experiência próxima da loja.

## Estrutura do projeto

- `index.html`: página inicial com apresentação, diferenciais e navegação
- `src/pages/historia.html`: história da família e da equipe
- `src/pages/catalogo.html`: lista de tipos e tabela de rótulos
- `src/pages/harmonizacoes.html`: dicas, link externo e vídeo do YouTube
- `src/pages/contato.html`: formulário de contato com nome, e-mail e mensagem
- `src/css/style.css`: estilo base com classes e ids + importa `efeitos.css` no final
- `src/css/efeitos.css`: pseudo-classes, pseudo-elementos, keyframes, transições e transformações (CP2), ligado via `<link>` em cada página
- `src/assets/imgs/`: pasta prevista para imagens locais (atualmente usamos imagens externas)
- `src/js/`: reservado para scripts futuros

## Integrantes

- Lucas Rocha Guerra — RM 576845

## Site publicado

- Repositório: https://github.com/lcs-rg/CP2-Front-End
- GitHub Pages: https://lcs-rg.github.io/CP2-Front-End/

## Efeitos Visuais

Direção: "bordô rico" — bordô `#7a1e2e` + dourado `#d9a441` sobre pergaminho suave `#e7d9bc` (sem brancos puros), com cabeçalho em degradê de adega. Sóbrio, com um risco: selo "🍷 desde 2010" com flutuação contínua e sublinhado do menu que enche como vinho na taça.

| Recurso | Onde | Como |
|---|---|---|
| `:hover` | Menu, `.btn`, `article`, `img` | Muda cor/sombra + `translateY(-2px/-4px)` e `scale(1.03)` nas imagens |
| `:focus-visible` / `:focus` | Links, botão, `input`, `textarea` | Anel dourado-escuro `outline` + campo clareia no foco |
| `:nth-child()` | Tabela do catálogo, `.lista-vinhos`, `article` | Zebrado `even/odd` em pergaminho, 2º item em destaque, `animation-delay` em cascata |
| `:not()` | `.menu li`, `.lista-vinhos li` | Espaço e filete tracejado em todos menos o último |
| `::after` | `.menu a` | Fio dourado em degradê com `scaleX(0→1)` no hover e na página atual |
| `::before` | `.destaque`, `h2` | Selo "🍷 desde 2010" flutuante + filete dourado antes dos títulos |
| `::selection` / `::first-letter` | Texto geral / história | Seleção bordô + capitular em Marcellus |
| `@keyframes fadeUp` | `.destaque`, `article` | Entrada `opacity 0→1` + `translateY(18px→0)` — recarregue a página para ver |
| `@keyframes pulseCta` | `.btn` | Brilho dourado suave a cada 3s |
| `@keyframes flutuarSelo` | `.destaque::before` | Selo oscila `rotate(35°→33°)` continuamente — visível sem hover |
| Transições | Todos interativos | `0.3s ease` em cor, fundo, sombra e transform |
| `scale()` | `main img:hover` | `scale(1.03)` — passe o mouse nas fotos |
| `translate()` + `rotate()` | `article`, `.btn`, `table tr`, selo | `translateY(-4px/-2px/-1px)` + `rotate(35°)` no selo |
| `prefers-reduced-motion` | Global | Desliga animação/transição se o usuário preferir |
