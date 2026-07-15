# Modo Scenes (Xiaohei 2.0) — condensado Grok

> Fonte completa: [ian-xiaohei-scenes](https://github.com/helloianneo/ian-xiaohei-scenes).  
> Use este arquivo quando o hub rotear para **scenes** e a skill irmã não estiver instalada.

## Fórmula

```text
Xiaohei + objeto real + ação física + rótulos curtos + vazio narrativo
```

Objetivo: o leitor vê um **mini-set real** (estúdio branco), depois em ~1s pensa “isso sou eu”.

**Não** é o whiteboard 1.0 (`style-dna.md` de illustrations). **Não** é página de PPT.

## Dois submodos

| Submodo | Formato Grok | Uso |
|---------|--------------|-----|
| **Padrão** | `image_gen` `aspect_ratio: "16:9"` | Um objeto + uma ação + 2–4 rótulos |
| **Long-scroll (easter egg)** | `aspect_ratio: "20:9"` no Grok (`21:9` e `2.6:1` não são válidos na API Imagine) | Trajetória: 5–8 nós de objeto real ao longo de uma curva |

## DNA visual 2.0 (padrão 16:9)

- Fundo **branco puro** `#FFFFFF` (estúdio), superfície clara.  
- **Objeto real** com luz/sombra unificada (não clipart, não UI screenshot).  
- **Um** conflito físico central (puxar, filtrar, bloquear, carimbar, afundar…).  
- Xiaohei **executa** a ação (mesmo critério de `xiaohei-ip.md`: se tirar ele e a cena “funciona sozinha”, falhou).  
- 2–4 rótulos manuscritos curtos (PT-BR ou chinês).  
- Acentos: azul / rosa / amarelo / verde / vermelho — só pontos de ritmo.  
- Sem PPT, sem setas de arquitetura, sem logo não autorizado, sem lista de elementos do tema.

## DNA long-scroll

- Fundo **quase branco** sofisticado (não cinza sujo).  
- Uma **curva preta fina** esquerda → direita.  
- 5–8 nós: cada um com objeto real + Xiaohei + 1–3 linhas de anotação.  
- Sem numeração tipo “passo 1–2–3”.  
- Fatos pessoais/marca: **só** o que o usuário deu (sem inventar biografia).  
- Substituir nós do exemplo oficial; não copiar trajetória do Ian.

## Extração de história (antes de desenhar)

1. Quem ressoa?  
2. O que puxa / filtra / pressiona / devolve o personagem?  
3. Qual **ação física** carrega isso?  
4. Qual **objeto real** carrega a ação?  
5. 2–4 palavras que batem na dor?

## Tipos de cena (guia, não template)

| Tipo de dor | Ação física típica | Objetos possíveis (reinventar) |
|-------------|-------------------|--------------------------------|
| Reunião / alinhamento puxa de volta | ser puxado por cabo/fio | cabo, cadeira de reunião, fone |
| Overload de mensagens | não conseguir segurar o fluxo | telefone, bilhetes, papelada |
| Alarme / produção / plantão | apagar fogo / pressionar sirene | sirene, relógio, cabo de rede |
| Review / retrabalho | carimbar / devolver | lupa, carimbo, pilha de papéis |
| Identidade / automação | trocar crachá / renomear | crachá, etiqueta, carimbo |
| Filtro / perda de oportunidade | peneirar / deixar cair | funil, peneira, currículos-papel |

**Anti-cópia:** aprenda proporção e peso visual dos exemplos oficiais; **não** clone props e pose.

## Prompt base (`image_gen` 16:9)

```text
16:9 Chinese/Portuguese article illustration, white studio #FFFFFF, real physical object mini-scene (product photo feel of one prop), not hand-drawn whiteboard diagram, not PPT.
Xiaohei: small solid-black absurd creature, white dot eyes, thin legs, deadpan — must perform the core physical action with the real object.
Scene: {objeto real} + {ação física clara em uma frase}.
Sparse 2-4 short handwritten labels in {pt-BR|Chinese}: {rótulos}.
Light accent dots blue/pink/yellow/green/red only for rhythm. Lots of empty white space. No screenshots, no UI, no logos, no flowchart arrows, no cute mascot, no dense text.
```

## Prompt long-scroll

```text
Ultra-wide panoramic story illustration, ultra-wide landscape scroll, refined near-white studio background.
A thin hand-drawn black curved path left to right with 5-8 uneven real-object story nodes (not a numbered timeline, not a PPT process).
At each node: real prop + Xiaohei doing a small physical action + 1-3 short handwritten notes in {pt-BR|Chinese}.
Start left: {início}. End right: {conclusão}. Facts only from user brief: {fatos}.
Clean, airy, photographic props, deadpan Xiaohei, no corporate infographic, no logos unless user provided.
```

## QA crítico (não entregar se falhar)

- Xiaohei na ação física.  
- Um objeto principal (não inventário do tema).  
- Parece mini-set real, não esboço 1.0 nem slide.  
- Rótulos curtos legíveis.  
- Não é clone de exemplo oficial.  
- Long-scroll: curva contínua, nós desiguais, fatos ancorados.

## Entrega

```text
assets/<slug>-scenes/
assets/<slug>-long-scroll/   # se long-scroll
```

Ferramentas Grok: `image_gen`, `image_edit` (remover título, reforçar ação), `read_file` para QA visual.
