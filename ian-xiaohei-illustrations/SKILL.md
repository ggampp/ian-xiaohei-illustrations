---
name: ian-xiaohei-illustrations
description: >
  Hub visual Ian no Grok Build: ilustrações Xiaohei 1.0 (whiteboard absurdo), cenas
  Xiaohei 2.0 (objeto real + ação física, incl. long-scroll) e páginas handdrawn-PPT
  (Capa 20:9 (Grok) + slides 16:9 em PNG). Use para artigos, posts, Notion, metodologia,
  comparação de produto, dor de trabalho, retrospectiva, curso, “faça um PPT”, shot list,
  capa, deck, “Xiaohei 2.0”, “cena com objeto real”. Roteia entre modos; ferramentas
  image_gen e image_edit. Repos: ian-xiaohei-illustrations, ian-xiaohei-scenes,
  ian-handdrawn-ppt (helloianneo).
metadata:
  short-description: "Hub Ian: Xiaohei 1.0 + Scenes 2.0 + Handdrawn PPT (Grok)"
---

# Ian Visual Hub — Illustrations · Scenes · Handdrawn PPT (Grok)

## Posicionamento

Esta skill é o **hub em português BR** para a família visual do Ian no **Grok Build**. Por padrão este repositório entrega o modo **Illustrations (Xiaohei 1.0)**, mas **deve contemplar e rotear** os projetos irmãos:

| Modo | Projeto | Repo |
|------|---------|------|
| `illustrations` | Ian Xiaohei Illustrations (1.0) | https://github.com/helloianneo/ian-xiaohei-illustrations |
| `scenes` | Ian Xiaohei Scenes (2.0) | https://github.com/helloianneo/ian-xiaohei-scenes |
| `handdrawn-ppt` | Ian Handdrawn PPT | https://github.com/helloianneo/ian-handdrawn-ppt |

> URL com typos tipo `ian-xiaohei-scenesssssssssss` → tratar como **ian-xiaohei-scenes**.

### Em uma frase por modo

- **Illustrations 1.0:** julgamento/fluxo/estrutura → rascunho de quadro absurdo, traço preto, fundo branco puro, rótulos vermelho/laranja/azul. Xiaohei na ação conceitual.  
- **Scenes 2.0:** situação humana → mini-set com **objeto real** + Xiaohei na ação física; opcional **long-scroll** de trajetória.  
- **Handdrawn PPT:** material → **páginas PNG** estilo explicação técnica à mão (Capa 20:9 (Grok), corpo 16:9). Xiaohei em geral **não** entra.

## Passo 0 — Roteamento (obrigatório)

Antes de gerar, leia `references/ecosystem-routing.md` e declare o modo de cada entrega:

```text
Modo: illustrations | scenes | handdrawn-ppt | híbrido
Submodo (se scenes): padrão 16:9 | long-scroll
Submodo (se ppt): Capa 20:9 (Grok) | corpo 16:9 | deck N páginas
```

| Pedido do usuário | Modo |
|-------------------|------|
| Fluxo, método, Clean Core, comparação de produto, whiteboard | `illustrations` |
| Dor, reunião, overload, “é sobre mim”, objeto real, Xiaohei 2.0 | `scenes` |
| Trajetória, retrospectiva, evolução do produto em friso | `scenes` + long-scroll |
| PPT, slides, curso, capa de artigo, deck | `handdrawn-ppt` |
| Artigo completo com capa + método + dor | **híbrido** (pastas separadas) |

Se ambíguo e a escolha mudar o resultado: **uma** pergunta curta. Senão, default = `illustrations`.

**Não misture DNAs no mesmo canvas** (traço 1.0 + props foto 2.0, ou slide com título de PPT dentro de illustrations).

## Runtime: Grok Build

| Situação | Ferramenta |
|----------|------------|
| Nova imagem | `image_gen` + `aspect_ratio` adequado |
| Editar | `image_edit` |
| QA visual | `read_file` na imagem |
| Consistência de personagem/deck | mesma descrição de IP/style lock; opcional ref em `image_edit` |

### Aspect ratios

| Modo | Ratio |
|------|-------|
| illustrations (corpo) | `16:9` |
| scenes (padrão) | `16:9` |
| scenes long-scroll | `20:9` (Grok; `21:9` inválido na API) |
| handdrawn-ppt capa | `20:9` (Grok; `21:9` inválido na API) |
| handdrawn-ppt corpo | `16:9` |

Orientação geral de prompt Imagine: skill `imagine` do Grok; **DNA do modo escolhido** tem prioridade.

## Mapa de referências

Leia **só o necessário** do modo ativo:

### Sempre (hub)

- `references/ecosystem-routing.md` — decisão de modo e híbridos.

### Modo `illustrations` (completo neste repo)

- `references/style-dna.md`
- `references/xiaohei-ip.md`
- `references/composition-patterns.md`
- `references/prompt-template.md`
- `references/qa-checklist.md`
- `assets/examples/` — calibração esporádica; não copiar composição.

### Modo `scenes` (condensado neste repo)

- `references/mode-scenes.md`
- Se a skill irmã existir em `~/.grok/skills/ian-xiaohei-scenes/`, **prefira o SKILL.md e references oficiais**.

### Modo `handdrawn-ppt` (condensado neste repo)

- `references/mode-handdrawn-ppt.md`
- Se existir `~/.grok/skills/ian-handdrawn-ppt/`, **prefira o pacote oficial**.

## Fluxos por modo

### A) Illustrations (1.0) — detalhe completo

1. Digestão → âncoras cognitivas.  
2. Shot list (se só planejar).  
3. `image_gen` 16:9 por âncora (template em `prompt-template.md`).  
4. QA `qa-checklist.md`; `image_edit` se preciso.  
5. Salvar em `assets/<slug>-illustrations/`.

Regras-chave: fundo branco puro; traço preto; Xiaohei na ação; ≤5–8 rótulos curtos; sem PPT; metáfora nova (não copiar `assets/examples/`).

### B) Scenes (2.0) — ver `mode-scenes.md`

1. Extrair **situação** + ação física + objeto real.  
2. Shot list com ressonância (não só estrutura).  
3. `image_gen` 16:9 (ou 20:9 long-scroll).  
4. QA: mini-set real, Xiaohei na ação, sem inventário de props.  
5. `assets/<slug>-scenes/` ou `…-long-scroll/`.

### C) Handdrawn PPT — ver `mode-handdrawn-ppt.md`

1. Intake + blueprint (título, ponto, arquétipo, texto exato).  
2. Style lock do deck em todos os prompts.  
3. Capa `20:9` + páginas `16:9`, uma `image_gen` cada.  
4. QA de consistência de deck e texto curto.  
5. `assets/<slug>-handdrawn-ppt/`.  
6. **Não** entregar PPTX salvo pedido explícito fora desta skill.

### D) Híbrido

Declarar tabela frame → modo. Gerar por modo. Pastas separadas. Entregar mapa:

```text
capa → handdrawn-ppt
01–04 → illustrations
05–06 → scenes
```

## Idioma

| Origem do texto | Rótulos / títulos na imagem |
|-----------------|----------------------------|
| PT-BR | Português curto |
| Chinês | Chinês curto |
| Misto | Idioma dominante do trecho |

Modelos de imagem falham com texto longo: **menos rótulos, mais estável**.

## Instalação no Grok

```powershell
# Hub (este repo)
$dest = Join-Path $env:USERPROFILE ".grok\skills\ian-xiaohei-illustrations"
Copy-Item -Recurse -Force ".\ian-xiaohei-illustrations" $dest
```

Opcional — skills irmãs completas:

```powershell
# Após clonar os repos oficiais
Copy-Item -Recurse -Force ".\ian-xiaohei-scenes\ian-xiaohei-scenes" (Join-Path $env:USERPROFILE ".grok\skills\ian-xiaohei-scenes")
Copy-Item -Recurse -Force ".\ian-handdrawn-ppt\ian-handdrawn-ppt" (Join-Path $env:USERPROFILE ".grok\skills\ian-handdrawn-ppt")
```

Com as três instaladas, o hub **roteia**; a execução profunda usa o pacote irmão se presente.

## Uso típico

```text
Use a skill ian-xiaohei-illustrations (hub Ian).
Para o texto abaixo: roteie o modo certo e gere as imagens no Grok.
Se for método → illustrations; se for dor/situação → scenes; se for deck → handdrawn-ppt.
```

```text
Modo scenes: 3 cenas Xiaohei 2.0 com objeto real sobre pressão de release.
```

```text
Modo handdrawn-ppt: 1 Capa 20:9 (Grok) + 4 páginas 16:9 sobre Clean Core.
```

```text
Híbrido: capa PPT + 3 illustrations de estrutura + 1 scene de manutenção.
```

## Tom da entrega

Antes: modo escolhido + shot list / blueprint curto.  
Depois: contagem, uso, caminhos, o que é estável vs opcional.  
Sem tratado longo de teoria — deixe a imagem falar.
