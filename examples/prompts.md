# Exemplos de prompt (Grok Build)

Copie no chat do Grok. A skill é um **hub**: roteia `illustrations` | `scenes` | `handdrawn-ppt` e usa `image_gen` / `image_edit`.

## Roteamento explícito

```text
Use a skill ian-xiaohei-illustrations (hub Ian).
Declare o modo e gere:
- illustrations para a parte de método
- scenes para a dor de manutenção
- handdrawn-ppt para 1 Capa 20:9 (Grok)

<cole o artigo>
```

## Modo Scenes 2.0 (objeto real)

```text
Use a skill ian-xiaohei-illustrations em modo scenes (Xiaohei 2.0).
Gere 3 ilustrações 16:9: objeto real + Xiaohei na ação física + 2–4 rótulos em português.
Temas: overload de mensagens; review que devolve trabalho; filtro que deixa a oportunidade cair.
Sem diagrama de quadro branco (isso é modo illustrations).
```

## Long-scroll (Scenes)

```text
Use a skill ian-xiaohei-illustrations em modo scenes long-scroll.
Uma imagem panorâmica (20:9 no Grok) da trajetória do projeto abaixo, 5–8 nós com objeto real.
Só use fatos deste brief; não invente biografia.

<cole a linha do tempo>
```

## Modo Handdrawn PPT

```text
Use a skill ian-xiaohei-illustrations em modo handdrawn-ppt.
1 Capa 20:9 (Grok) + 4 páginas 16:9 sobre o texto abaixo.
Style lock de papel quase branco, traço fino, pastéis; texto curto na imagem.
Não gere arquivo PPTX — só PNGs de página.

<cole o material>
```

---

# Modo Illustrations 1.0 (padrão)

A skill usa `image_gen` (`aspect_ratio: "16:9"`) e `image_edit` para correções.

## Só planejar

```text
Use a skill ian-xiaohei-illustrations — ainda não gere imagens.
Analise o artigo abaixo e monte um shot list com cerca de 5 ilustrações.
Para cada uma: parágrafo-alvo, tema, ideia central, tipo de estrutura,
ação do Xiaohei, elementos e rótulos curtos em português.

<cole o artigo>
```

## Gerar ilustrações do corpo

```text
Use a skill ian-xiaohei-illustrations e gere 4 ilustrações absurdas do Xiaohei
para o artigo abaixo. 16:9, fundo branco puro, traço preto à mão,
poucas anotações manuscritas em português (vermelho/laranja/azul).
Uma ideia por imagem; sem PPT e sem cartoon fofo. Use image_gen.

<cole o artigo>
```

## Texto longo — só estratégia

```text
Use a skill ian-xiaohei-illustrations para a estratégia de ilustração deste texto longo.
Não distribua figuras de forma uniforme: só âncoras cognitivas
(julgamento, loop entrada/saída, antes/depois, armadilhas, handoff).
6–8 itens no shot list; sem gerar ainda.

<cole o artigo>
```

## Uma ideia → uma imagem

```text
Use a skill ian-xiaohei-illustrations e gere uma ilustração 16:9 para:

Confiança não se grita: se constrói evidência por evidência.

Absurdo mas limpo; Xiaohei na ação central; no máximo 5 rótulos curtos em português.
```

## Tema de workflow

```text
Use a skill ian-xiaohei-illustrations: uma imagem para
“transformar material bruto em conteúdo de tráfego, confiança e conversão”.
Sem fluxograma formal e sem reciclar o peixe multi-uso dos exemplos.
Metáfora low-tech nova; Xiaohei na ação central.
```

## Editar: remover título

```text
Use a skill ian-xiaohei-illustrations e image_edit nesta imagem:
remova o título “Workflow / fluxograma” e o sublinhado no canto superior esquerdo.
Resto idêntico; não adicione texto nem objetos.
```

## Editar: mais Xiaohei

```text
Use a skill ian-xiaohei-illustrations: a direção está certa, mas o Xiaohei parece decoração.
Regenere (image_edit ou image_gen) com a mesma ideia — Xiaohei deve fazer a estrutura funcionar.
Mais absurdo, branco puro, limpo, pouco texto.
```

## Lote de amostras de estilo

```text
Use a skill ian-xiaohei-illustrations e gere 5 ilustrações 16:9 do Xiaohei, uma por chamada image_gen.
Temas: sobrecarga de informação; validação de produto; juros compostos de conteúdo;
empresa de uma pessoa; construção de confiança.
Não junte em um único canvas.
```

## Artigo em chinês (rótulos em chinês)

```text
Use a skill ian-xiaohei-illustrations e gere 3 ilustrações 16:9 do Xiaohei para o artigo em chinês abaixo.
Anotações manuscritas curtas em chinês; DNA visual padrão (branco, traço à mão).

<cole o artigo>
```
