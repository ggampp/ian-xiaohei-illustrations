# Modo Handdrawn PPT — condensado Grok

> Fonte completa: [ian-handdrawn-ppt](https://github.com/helloianneo/ian-handdrawn-ppt).  
> Use quando o hub rotear para **páginas tipo PPT / capa / deck**.  
> “PPT” aqui = **PNG de página inteira**, não `.pptx` editável.

## Posicionamento

Transformar artigo, outline, notas ou ideia em **deck de imagens** estilo explicação técnica à mão (chinês ou PT-BR):

1. Intake do material  
2. Narrativa do deck  
3. Arquétipo por página  
4. DNA visual travado  
5. Uma `image_gen` por página  
6. Contact sheet se multipágina  

**Fora de escopo:** PPTX/PDF/Keynote editáveis como entrega principal.

## Formatos Grok

| Papel da página | `aspect_ratio` |
|-----------------|----------------|
| Capa de artigo / blog | `"20:9"` no Grok (`21:9` não é aceito) |
| Corpo / slide padrão | `"16:9"` |

## DNA visual (V6 condensado)

- Papel **quase branco** (não amarelo, não marrom craft).  
- **Sem** moldura de slide grossa em volta da página (padrão moderno).  
- Linhas finas à mão, hachura leve a lápis.  
- Pastéis: azul claro, verde sálvia, pêssego, lavanda — marcas suaves.  
- Diagrama **central pequeno**; muito espaço negativo.  
- Título **contido** (não poster de marketing).  
- Texto na imagem: **curto, exato, listado no prompt** (`Required text only`).  
- Personagens: no máximo um leitor/engenheiro discreto; **Xiaohei não é obrigatório** (e em geral não entra).  
- Consistência de deck: mesmo tom de papel, mesma “casca” (posição de título, peso de linha, escala).

## Arquétipos de página (escolha por semântica)

| Arquétipo | Conteúdo típico |
|-----------|-----------------|
| Capa / metáfora | Uma imagem-ideia + título curto |
| Esquerda/direita | Contraste A vs B |
| Fluxo | 3–5 etapas leves (não arquitetura SAP densa) |
| Ciclo | Loop de processo |
| Classificação | 3–4 caixas leves |
| Matriz | 2×2 simples |
| Lista numerada curta | Método em 3 perguntas |
| Resumo | 3 bullets + ícone central |

Varie arquétipos no deck; não repita o mesmo layout em todas as páginas.

## Workflow

### 1. Intake

Tema, público, cena de uso (artigo / curso / pitch), comprimento alvo, suficiência do material.  
No máximo 1–3 perguntas se faltar o que muda o deck.

### 2. Blueprint (sempre mental; escrito se pedirem só planejamento)

Para cada página:

- título  
- ponto único  
- arquétipo  
- texto visível exato (curto)  
- brief do diagrama  

Defaults: artigo 8–12 páginas; ideia curta 5–8; módulo de curso 15–30 (confirmar com usuário).

### 3. Style lock do deck (colar em todo prompt)

```text
Deck style lock: near-white paper background, refined Chinese/Portuguese handdrawn technical explanation style, thin wobbly pen lines, light pencil hatching, soft pastel marks (light blue, sage, peach, lavender), large negative space, small central diagram, restrained title, no heavy slide border, no corporate PowerPoint template, no glossy 3D, no photoreal stock photo collage. Consistent title block position and line weight across pages.
```

### 4. Geração

- Uma página = uma `image_gen`.  
- Capa: `20:9`. Corpo: `16:9`.  
- Incluir lista **Required text only** com as strings exatas.  
- Se o texto sair errado: reduzir palavras → regenerar; ou aceitar composição e anotar risco (pós-processo tipográfico fica fora se o usuário não pedir).

### 5. Contact sheet (multipágina)

Se o usuário quiser visão geral: montar grade com shell (HTML/imagem) **ou** listar paths em ordem. Opcional; não bloqueia entrega.

## Prompt de página (corpo 16:9)

```text
{Deck style lock}

Page role: body illustration 16:9 handdrawn technical explanation page.
Main point: {um ponto}.
Layout archetype: {arquétipo}.
Central diagram brief: {descrição curta do desenho}.
Required text only (exact, short, handwritten-technical look):
- Title: "{título}"
- Labels: "{a}", "{b}", "{c}"
No extra paragraphs. No Xiaohei unless user asked. Clean, airy, one idea.
```

## Prompt de capa (20:9 no Grok)

```text
{Deck style lock}

Page role: ultra-wide article cover.
One strong metaphor diagram centered or slightly left; restrained title; generous empty paper.
Required text only:
- Title: "{título}"
- Optional subtitle: "{subtítulo curto ou vazio}"
Not a body slide. Not a busy infographic.
```

## QA

- Uma ideia por página.  
- Texto curto e (na medida do possível) legível.  
- Mesmo DNA em todo o deck.  
- Capa não parece slide de corpo (e vice-versa).  
- Sem “template PowerPoint roxo/azul corporativo”.  
- Sem prometer PPTX.

## Entrega

```text
assets/<slug>-handdrawn-ppt/
  cover-....png|jpg
  page-01-....png|jpg
  ...
```

Relatar: pasta, contagem, tipo de deck, premissas, riscos de texto no modelo de imagem.
