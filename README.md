# Vayron Eyewear — site

**Site no ar:** https://jfrancomelo-eng.github.io/vayron-eyewear/

## Conceito

A Vayron é uma ótica online do Recife, com armações autorais e laboratório próprio de lentes (New Lab). O site funciona como uma **vitrine premium**: apresenta as armações como peças de design, mostra como a lente é feita e leva o cliente ao atendimento no WhatsApp, onde o pedido é fechado.

A ideia central é passar a confiança de uma loja física num atendimento 100% online. Por isso o site mostra o produto em detalhe (vídeo, 3D, medidas e materiais) e explica o processo do começo ao fim.

## Como o site é feito (base)

| Parte | Tecnologia |
|---|---|
| Página | Um único `index.html` com HTML, CSS e JavaScript puros, sem framework e sem etapa de build |
| 3D | Three.js 0.128 (CDN), com o modelo da armação Áurea |
| Vídeos | `media/abertura.mp4` e `media/vitrine.mp4` (MP4 H.264), renderizados do modelo 3D, não gerados por IA |
| Imagens | `img/*.webp`, três vistas de cada armação (frente, ¾ e lado) |
| Fontes | Manrope e Michroma (Google Fonts) |
| Contato | Links diretos para o WhatsApp com mensagem pronta para cada armação |
| Hospedagem | GitHub Pages (site estático) |

## Seções da página

1. **Abertura** com o vídeo da armação.
2. **Vitrine** das armações autorais, com fotos e pedido pelo WhatsApp.
3. **Detalhes da peça**: metal polido, ferragens e a assinatura da marca.
4. **Lentes**: como saem do laboratório, montagem e ajuste.
5. **Prove as lentes**: comparação de tipos de lente.
6. **Medidas e provador**: como medir e escolher o tamanho certo.
7. **Comprar online**: passo a passo do pedido ao recebimento.
8. **Atendimento** completo pelo WhatsApp e pelo Instagram.

## Estrutura

```
index.html      página completa (estilo e scripts embutidos)
img/            fotos das armações (.webp)
media/          vídeos da abertura e da vitrine + imagens de capa
_headers        cabeçalhos de cache/segurança (Netlify/Cloudflare; o GitHub Pages ignora)
iniciar-servidor.bat   abre um servidor local no Windows
```

## Rodar no computador

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000`. No Windows, também dá para dar dois cliques em `iniciar-servidor.bat`.
