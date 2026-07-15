# Ian Xiaohei Illustrations (hub visual Ian)

> Transforme julgamentos, fluxos, estados e metáforas de um artigo em ilustrações de corpo de texto: fundo branco, traço à mão, absurdas mas limpas.
>
> 16:9 horizontal | IP Xiaohei 1.0 | mão livre em branco puro | poucas anotações vermelho/laranja/azul | **Grok Build** (`image_gen` / `image_edit`)
>
> **Hub:** também roteia e executa (modo condensado) **[Xiaohei Scenes 2.0](https://github.com/helloianneo/ian-xiaohei-scenes)** e **[Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt)**.

---

## O que é este repositório

**Ian Xiaohei Illustrations** é uma skill de agente para projetar e gerar ilustrações de corpo de texto (artigos, posts, blogs, Notion, metodologias) no estilo **Xiaohei 1.0** (rascunho de quadro).

Neste fork local (PT-BR + Grok), o pacote funciona como **hub da família visual Ian**:

| Modo | Projeto | Quando |
|------|---------|--------|
| `illustrations` | Este repo (1.0) | Método, fluxo, estrutura, comparação de produto |
| `scenes` | [ian-xiaohei-scenes](https://github.com/helloianneo/ian-xiaohei-scenes) (2.0) | Situação humana, objeto real, long-scroll de trajetória |
| `handdrawn-ppt` | [ian-handdrawn-ppt](https://github.com/helloianneo/ian-handdrawn-ppt) | Capa 20:9 (Grok) + páginas PNG “tipo PPT” (não gera PPTX) |

O agente **escolhe o modo** (`references/ecosystem-routing.md`) e usa DNA/prompt do modo ativo. Com as skills irmãs instaladas em `~/.grok/skills/`, preferir o pacote oficial completo.

Não é prompt genérico nem template de infográfico. No 1.0 o fluxo é: achar a **âncora cognitiva** e desenhar **um** julgamento/fluxo/metáfora em 16:9.

IP padrão (modos Xiaohei): **小黑** — preto sólido, olhos brancos, pernas finas, expressão vazia; **faz a ação central**, não decora.

Em uma frase (1.0): **o agente não “coloca uma figurinha” — desenha o movimento cognitivo do texto.**

---

## Para quem serve

**Serve para:**

- quem escreve artigos e precisa de ilustrações de corpo de texto  
- conteúdo de conhecimento, metodologia e workflows de IA  
- transformar julgamento abstrato em metáfora concreta  
- estilo mais leve e estranho que PPT, com identidade  
- quem usa **Grok** e quer reutilizar uma linguagem visual estável  

**Não serve para:**

- ilustração comercial / KV de marca  
- fluxograma formal ou arquitetura densa  
- cartoon infantil / mascote fofo  
- despejar parágrafo inteiro ou “página de curso” numa imagem  
- precisar de SVG editável de produção  

---

## O que entrega

**Padrão:**

- ilustrações **16:9**  
- shot list de **4–8** itens por artigo  
- tema, ideia, estrutura, ação do Xiaohei e rótulos sugeridos  
- PNG via `image_gen`, organizados em `assets/<slug>-illustrations/`  

**Não entrega por padrão:**

- PPTX / PDF / Keynote  
- SVG / HTML editável  
- poster comercial  
- infográfico cheio de texto  

---

## Estilo visual

- fundo **branco puro** (sem textura, sombra, gradiente)  
- traço preto à mão, linha fina, leve tremer  
- muito vazio; sujeito ~40–60% do quadro  
- poucas anotações manuscritas (PT-BR ou chinês conforme o texto) em vermelho / laranja / azul  
- uma imagem = um núcleo  
- Xiaohei na ação central  
- absurdo e limpo — não infantil  

---

## Exemplos de estilo

### Dois breakpoints

![Dois breakpoints](examples/images/01-two-breakpoints.png)

### Separar por propósito

![Separar por propósito](examples/images/02-sort-by-purpose.png)

### Um peixe, vários usos

![Um peixe, vários usos](examples/images/03-one-fish-many-uses.png)

### Caminho de handoff

![Caminho de handoff](examples/images/04-handoff-path.png)

### Poço de informação

![Poço de informação](examples/images/05-information-well.png)

### Prensa de ideias

![Prensa de ideias](examples/images/06-idea-press.png)

### Fermentação de conteúdo

![Fermentação de conteúdo](examples/images/07-content-fermentation.png)

### Ponte de confiança

![Ponte de confiança](examples/images/08-trust-bridge.png)

Estas imagens calibram densidade de traço, vazio, cor e participação do Xiaohei. **Não** copie composição nem objetos — invente metáfora nova a cada artigo.

---

## Instalação no Grok Build

Clone o repositório:

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copie a skill para a pasta de skills do Grok:

**Windows (PowerShell):**

```powershell
$dest = Join-Path $env:USERPROFILE ".grok\skills\ian-xiaohei-illustrations"
New-Item -ItemType Directory -Force -Path (Split-Path $dest) | Out-Null
Copy-Item -Recurse -Force ".\ian-xiaohei-illustrations" $dest
```

**macOS / Linux:**

```bash
mkdir -p "${HOME}/.grok/skills"
cp -R ./ian-xiaohei-illustrations "${HOME}/.grok/skills/"
```

O pacote instalável é o subdiretório:

```text
ian-xiaohei-illustrations/
```

(README, LICENSE, NOTICE e `examples/` na raiz são documentação do repositório.)

Uso no chat:

```text
Use a skill ian-xiaohei-illustrations e gere 5 ilustrações absurdas do Xiaohei
para este artigo em português (16:9, image_gen).
```

### Codex (legado)

Ainda é possível copiar o mesmo diretório para `${CODEX_HOME:-$HOME/.codex}/skills/`. O `SKILL.md` atual prioriza o runtime **Grok** (`image_gen` / `image_edit`).

---

## Como usar

### Só planejar

```text
Use a skill ian-xiaohei-illustrations — não gere ainda.
Analise o artigo e entregue um shot list (~5 imagens):
parágrafo, tema, ideia, estrutura, ação do Xiaohei, rótulos.

<cole o artigo>
```

### Gerar direto

```text
Use a skill ian-xiaohei-illustrations e gere 4 ilustrações do Xiaohei.
16:9, fundo branco, traço à mão, poucas anotações em português.

<cole o artigo>
```

### Um conceito

```text
Use a skill ian-xiaohei-illustrations: uma ilustração 16:9 para
“confiança se constrói evidência por evidência”.
Xiaohei na ação central; absurdo e limpo.
```

### Editar (image_edit)

```text
Use a skill ian-xiaohei-illustrations e edite a imagem:
remova o título “Fluxograma” no canto superior esquerdo; resto igual.
```

Mais exemplos: [examples/prompts.md](examples/prompts.md).

---

## Ferramentas Grok

| Tarefa | Ferramenta |
|--------|------------|
| Nova ilustração | `image_gen` + `aspect_ratio: "16:9"` |
| Corrigir / reforçar Xiaohei / tirar título | `image_edit` |
| Inspecionar resultado | `read_file` na imagem |
| Consistência no lote | mesma descrição de IP; opcional: 1ª imagem como referência em `image_edit` |

Fluxo resumido:

1. Ler o texto e achar âncoras cognitivas  
2. Shot list (se for só estratégia)  
3. Para cada imagem: prompt do template + `image_gen` 16:9  
4. QA (`references/qa-checklist.md`); `image_edit` se precisar  
5. Salvar em `assets/<slug>-illustrations/`  
6. Reportar caminhos e uso  

---

## Ecossistema (hub)

```text
Pedido → ecosystem-routing.md → modo
  illustrations → style-dna + prompt-template + …
  scenes        → mode-scenes.md  (± skill irmã completa)
  handdrawn-ppt → mode-handdrawn-ppt.md (± skill irmã completa)
  híbrido       → pastas separadas por modo
```

Aspect ratios no Grok: corpo 16:9 · capa PPT / long-scroll 20:9 (Grok).

---

## Estrutura do repositório

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   └── prompts.md
└── ian-xiaohei-illustrations/          ← skill instalável (hub)
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── ecosystem-routing.md      ← roteador 1.0 / 2.0 / PPT
        ├── mode-scenes.md            ← Scenes 2.0 condensado (Grok)
        ├── mode-handdrawn-ppt.md     ← Handdrawn PPT condensado (Grok)
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

---

## Cuidados

- Rótulos curtos geram texto mais estável no modelo de imagem.  
- Uma ideia por figura (ou por página, no modo PPT).  
- Nos modos Xiaohei: se tirar o personagem e a metáfora ainda “funciona sozinha”, regenere.  
- Exemplos = calibração, não molde.  
- Não misture DNA 1.0 (traço) com 2.0 (props foto) no mesmo canvas.  
- Espere typos ocasionais; se piorar, **reduza** o texto e regenere.  

---

## Projetos relacionados (família Ian)

- [Ian Xiaohei Scenes](https://github.com/helloianneo/ian-xiaohei-scenes) — Xiaohei 2.0, objeto real + long-scroll  
- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — páginas PNG estilo PPT técnico à mão  
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills)  
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain)  

---

## Sobre o autor

**Ian (伊恩)** — designer de produto / one-person company / AI builder  

- GitHub: [helloianneo](https://github.com/helloianneo)  
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)  
- Site: [www.ianneo.xyz](https://www.ianneo.xyz)  
- WeChat: `ianneoxyz`  
- E-mail: hello.neoc@gmail.com  

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="QR WeChat do Ian" width="120">
</p>

---

## Licença

MIT License. Ver [LICENSE](LICENSE).
