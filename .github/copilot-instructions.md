# Copilot Instructions — Pede Aí

Purpose: make AI agents productive immediately on this repo.

## Overview
- Static landing page for “Pede Aí” (AI via WhatsApp for obras).
- Single file app: `index.html` with inline CSS. No JS, no external libs.
- Language: PT-BR copy throughout. Tone: minimalista/GenZ, leve, direto.

## Architecture & Conventions
- One HTML document only. Avoid duplicar `<!DOCTYPE html>`/`<html>` blocks.
- Styles inline in `<style>`. Keep classes and patterns:
  - Layout: `.container` (max 960px), `.grid.two` (1→2 col em ≥768px), `.card`.
  - UI bits: `.features` (lista com ✓), chat bubbles `.bubble.me` / `.bubble.ai`.
  - Modals CSS-only: anchors para `#modal-*` + `.modal:target` para abrir.
  - Favicon: inline SVG via `link rel="icon"` data URL.
- Aesthetic: gradiente `--bg1:#667eea` → `--bg2:#764ba2`, emojis, hover suave.
- Cross-browser: quando usar `-webkit-background-clip:text`, também manter `background-clip:text`.

## Key Sections in `index.html`
- `#inicio` (hero + chat simulado) — call-to-actions “Quero testar” e “Como funciona”.
- `#como` — 4 cards (falar no Whats, IA organiza, alertas, CSV diário).
- `#whatsapp` — texto “Por que a interface é 100% WhatsApp” + comparação “Jeito antigo” vs “Com o Pede Aí”.
- `#beneficios` — lista curta e direta.
- `#precos` — “Como funciona a cobrança”: Plano Piloto (lista) e Plano Multiobras “Em breve”.
- `#contato` — formulário simples (nome, Whats, mensagem opcional) + botão WhatsApp.
- Footer — link WhatsApp `https://wa.me/554299110955` e ícones (LinkedIn/Instagram/Facebook placeholders).

## Developer Workflow
- No build/tooling. Preview local rápido:
  - `python3 -m http.server 8000` → abrir `http://localhost:8000`.
- Deploy: GitHub Pages.
  - Opção simples: Settings → Pages → Source: `Deploy from a branch` (`main` / root).
  - Este repositório possui `.github/workflows/jekyll-docker.yml` (legado). Caso Pages use GitHub Actions, pushes na `main` devem publicar a raiz do repositório. Se falhar, confira Settings → Pages (Source: GitHub Actions vs Branch).

## Editing Guidelines
- Mantenha um único documento HTML. Se reescrever, substitua todo o arquivo (não concatene).
- Não adicionar JS/bibliotecas externas sem pedido explícito.
- Preserve o tom PT-BR e o visual minimalista. Evite copiar textos do README antigo — a verdade é o `index.html` atual.
- Ao criar novas modais, siga o padrão:
  - Link: `<a href="#modal-exemplo">abrir</a>`
  - Estrutura: `<div id="modal-exemplo" class="modal"><div class="modal-box">…</div></div>`
- Novas seções: use `.section` implícita por `<section>`, `.grid.two` para 2 colunas responsivas, `.card` para blocos.

## Examples
- Novo item em “Jeito antigo”/“Com o Pede Aí”:
  - `<ul class="features"><li>Texto objetivo</li> …</ul>`
- Novo CTA estilo hero:
  - `<a class="cta" href="#contato">Chamar</a>` ou `<a class="cta alt" href="#como">Detalhes</a>`.

## Gotchas
- Erro frequente: HTML duplicado colado dentro do `<style>` → quebra linters. Garanta fechamento único `</html>` e nada após.
- Gradiente com texto: inclua `background-clip:text` e `-webkit-background-clip:text`.
- Conteúdo é PT-BR; mantenha acentos/aspas corretos e emojis.

## Scope for Agents
- É seguro rodar comandos locais (ex.: servidor HTTP). Não há dependências.
- Mudanças comuns: ajustar copy/estilo, adicionar seções, links de redes, ícones SVG inline, links de WhatsApp.
