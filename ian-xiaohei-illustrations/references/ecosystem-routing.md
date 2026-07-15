# Ecossistema Ian — roteamento visual

Três skills irmãs do autor [Ian (helloianneo)](https://github.com/helloianneo). Esta skill (**ian-xiaohei-illustrations**) é o **hub no Grok**: decide o modo certo e executa com as ferramentas `image_gen` / `image_edit`.

| Skill | Repo | Versão / papel | Visual | Quando usar |
|-------|------|----------------|--------|-------------|
| **Illustrations** (padrão desta skill) | [ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) | Xiaohei **1.0** | Traço à mão em **branco puro**, diagrama-metáfora, rótulos vermelho/laranja/azul | Método, fluxo, estrutura, julgamento, comparação de produto, Clean Core, arquitetura conceitual |
| **Scenes** | [ian-xiaohei-scenes](https://github.com/helloianneo/ian-xiaohei-scenes) | Xiaohei **2.0** | **Objeto real** + Xiaohei + ação física + vazio (estúdio branco) | Situação humana, ansiedade, rework, reunião, overload, ressonância “é sobre mim”, metáfora de vivência |
| **Handdrawn PPT** | [ian-handdrawn-ppt](https://github.com/helloianneo/ian-handdrawn-ppt) | Páginas técnicas à mão (sem Xiaohei obrigatório) | Papel quase branco, linhas finas, pastéis, título + diagrama de página inteira | Capa 20:9 (Grok), deck de curso, “faça um PPT”, página de explicação técnica densa, contact sheet multipágina |

## Decisão rápida

```text
Usuário quer PPT / slides / capa de artigo / deck de curso?
  → modo handdrawn-ppt

Usuário quer “cena real”, “objeto físico”, “situação de trabalho”, “long-scroll”, “história de projeto”, “Xiaohei 2.0”?
  → modo scenes
  → se também “long-scroll / trajetória / evolução do produto” → scenes + submodo long-scroll

Usuário quer “explicar estrutura / fluxo / método / contraste de produto” em rascunho de quadro?
  → modo illustrations (padrão)

Mistura (ex.: artigo com método + dor humana)?
  → shot list híbrido: marcar cada frame com modo illustrations | scenes
  → opcional: 1 capa handdrawn-ppt 20:9 + corpos illustrations ou scenes
```

## Sinais de gatilho (PT-BR e originais)

### → Illustrations (1.0)

- fluxograma conceitual, metodologia, framework, loop I/O, antes/depois de sistema  
- “diagrama absurdo”, “whiteboard”, “rascunho de produto”  
- comparação técnica (ex.: RAP vs Tachyonix, Clean Core)  
- shot list de âncoras **cognitivas**

### → Scenes (2.0)

- “é sobre mim”, dor do trabalhador, pressão, reunião, mensagem, revisão, filtro de currículo  
- objeto real (telefone, cadeira, crachá, ampulheta, cabo…)  
- “Xiaohei 2.0”, “cena física”, “estúdio com props”  
- long-scroll / trajetória / retrospectiva de projeto / evolução de produto  

### → Handdrawn PPT

- “faça um PPT”, slides, curso, workshop, capa de blog, deck  
- muitas páginas com título + um conceito por página  
- menos foco no Xiaohei; mais na **página técnica** com tipografia curta  

## O que **não** misturar no mesmo canvas

| Evitar | Por quê |
|--------|---------|
| Traço 1.0 + props fotográficos 2.0 na mesma figura | DNA conflita (esboço vs estúdio) |
| Cara de PPT do handdrawn-ppt dentro de illustrations | Illustrations **proíbe** título de tipo e moldura de slide |
| Xiaohei mascote no handdrawn-ppt | PPT mode raramente usa personagem; no máximo um leitor/engenheiro discreto |

## Híbridos recomendados (artigo longo)

1. **Capa** `handdrawn-ppt` 21:9 (metáfora do tema).  
2. **Corpo metodológico** `illustrations` 16:9 (âncoras de sistema).  
3. **Corpo de dor/situação** `scenes` 16:9 (1–2 cenas de ressonância).  
4. **Opcional** long-scroll `scenes` se for case/retrospectiva.

Entregue pastas separadas:

```text
assets/<slug>-illustrations/
assets/<slug>-scenes/
assets/<slug>-handdrawn-ppt/
assets/<slug>-long-scroll/   # se houver
```

## Aspect ratios no Grok Imagine

| Uso | Ratio válido |
|-----|----------------|
| Corpo illustrations / scenes / ppt | `16:9` |
| Capa handdrawn-ppt / long-scroll scenes | `20:9` ou `19.5:9` |
| **Inválido** | `21:9` (HTTP 422 na API) |

## Skills instaladas vs modo embutido

| Situação | Ação |
|----------|------|
| Só esta skill no Grok | Use os modos em `mode-scenes.md` e `mode-handdrawn-ppt.md` (condensados PT-BR + Grok) |
| Skills irmãs clonadas em `~/.grok/skills/` | Prefira o `SKILL.md` completo da irmã; este hub só roteia |
| Usuário cita o repo errado (`ian-xiaohei-scenessss…`) | Trate como **ian-xiaohei-scenes** |

## Prioridade se o usuário for ambíguo

1. Se disse **PPT / slides / capa** → handdrawn-ppt.  
2. Se a emoção/situação domina o texto → scenes.  
3. Caso contrário → **illustrations** (padrão deste repositório).  
4. Em dúvida em 1 pergunta curta: “Quer rascunho de quadro (1.0), cena com objeto real (2.0) ou páginas tipo PPT?”
