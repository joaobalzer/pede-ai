# Pede Aí - Landing Page

Uma landing page completa e responsiva para o produto "Pede Aí", um agente de IA via WhatsApp para automatização de pedidos de materiais em obras de construção.

## 🚀 Deploy

Esta é uma página estática que pode ser hospedada em qualquer serviço de hospedagem estática:

### GitHub Pages (Recomendado)
1. Faça push do código para o repositório GitHub
2. Vá em Settings → Pages
3. Selecione "Deploy from a branch"
4. Escolha a branch `main` e pasta `/ (root)`
5. Aguarde alguns minutos e acesse via URL fornecida

### Outros serviços de deploy
- **Netlify**: Arraste a pasta ou conecte o repositório GitHub
- **Vercel**: Conecte o repositório GitHub ou use a CLI
- **GitHub Codespaces**: Use o Simple Browser para preview local

## 📁 Estrutura

```
pede-ai/
├── index.html          # Arquivo principal (página completa)
└── README.md           # Este arquivo
```

## ✨ Características

- **Single Page Application**: Tudo em um arquivo HTML
- **Responsivo**: Mobile-first design
- **Sem dependências**: Apenas HTML + CSS puro
- **SEO-friendly**: Estrutura semântica HTML5
- **Rápido**: Sem carregamentos externos

## 🎨 Design

- **Paleta de cores**: Azul bebê (#87ceeb) + Azul escuro (#1a3a52)
- **Estilo**: "Construtora anos 90" - clean e profissional
- **Typography**: Fontes do sistema
- **Layout**: Container centralizado (máx. 1200px)

## 📱 Seções

1. **Início** (#inicio) - Hero com simulação de chat WhatsApp
2. **Como funciona** (#como-funciona) - Fluxo em 4 passos
3. **Dores de hoje** (#dores) - Problemas atuais na obra
4. **Benefícios** (#beneficios) - Vantagens do produto
5. **Por que WhatsApp** (#whatsapp) - Comparativo antes/depois
6. **Para quem** (#para-quem) - Público-alvo
7. **Como funciona por trás** (#por-tras) - Detalhes técnicos
8. **Casos reais** (#casos) - Cenários de uso
9. **Preços** (#precos) - Planos e valores
10. **FAQ** (#faq) - Perguntas frequentes
11. **Contato** (#contato) - Formulário para contato

## 🔧 Desenvolvimento Local

Para testar localmente:

```bash
# Clone o repositório
git clone <seu-repo>
cd pede-ai

# Inicie servidor local
python3 -m http.server 8000

# Acesse http://localhost:8000
```

## 📝 Customização

Para personalizar:
1. Edite o arquivo `index.html`
2. Modifique o CSS na seção `<style>` dentro do `<head>`
3. Ajuste textos, cores e imagens conforme necessário
4. Teste localmente antes do deploy

---

**Desenvolvido para automatizar pedidos na obra via WhatsApp** 🏗️📱