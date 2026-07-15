# Checklist de QA (Grok)

## Obrigatório (pass)

- **16:9** horizontal.
- Fundo **branco limpo**.
- Tem **Xiaohei**.
- Xiaohei na **ação central** (não só decoração).
- Metáfora **nova** para o artigo (não clone de exemplo).
- Absurdo, criativo, interessante.
- Limpo: sujeito ≤ ~**60%** do quadro.
- **Um** núcleo estrutural por imagem.
- Rótulos **poucos, curtos, legíveis** (PT-BR ou chinês).
- Laranja só em fluxo/setas; vermelho em alerta; azul em secundário.

## Sinais de falha → ação no Grok

| Sinal | Ferramenta sugerida |
|-------|---------------------|
| Título no canto | `image_edit` — remover só o título |
| Xiaohei fofo / canto | `image_edit` ou nova `image_gen` |
| Cara de PPT / curso | regenerar com template “simplificar” |
| Elementos/setas demais | regenerar com menos nós |
| Texto longo ou ilegível | regenerar com ≤3–5 rótulos curtos |
| Fundo sujo / textura | regenerar reforçando pure white |
| Parecido com `assets/examples/` | regenerar trocando objeto + ação |
| Precisa inspecionar texto/estilo | `read_file` na imagem gerada |

## Como iterar

- **Comum demais:** Xiaohei sujeito + metáfora estranha coerente.  
- **Complexo:** um movimento, 3–5 rótulos.  
- **Fofo:** deadpan, not cute, not mascot.  
- **PPT:** sem título, grade, setas em excesso.  
- **Clone de exemplo:** mesma ideia, outro objeto e outra ação.  
- **Texto errado:** edição local; se piorar, regenerar com menos texto.

## Entrega

Bom: o leitor pensa “que estranho…” e em ~1s entende a estrutura.

Ruim: parece página de tutorial em vez de rascunho absurdo de produto no papel branco.

## Entrega no workspace

- Listar caminhos retornados pelo Grok (`images/…` ou path absoluto).  
- Se o projeto pedir: copiar para `assets/<slug>-illustrations/01-….png`.  
- Não sobrescrever assets sem confirmação.
