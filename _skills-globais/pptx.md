---
name: pptx
description: >
  Cria apresentações PowerPoint (.pptx) com layouts e formatação profissional.
  Use para apresentações para clientes, decks de vendas, materiais de treinamento.
---

# /pptx — Criar Apresentação PowerPoint

## Input

O usuário fornece:
- Tema ou objetivo da apresentação
- Público-alvo (cliente, equipe, investidor)
- Conteúdo ou briefing
- Número de slides desejado (opcional)

## Workflow

1. Entender o objetivo e o público
2. Definir a estrutura de slides (mostrar ao usuário antes de criar)
3. Escrever o conteúdo de cada slide
4. Converter para .pptx usando python-pptx ou pandoc:

```bash
# Via pandoc
pandoc input.md -o output.pptx

# Se não tiver pandoc instalado:
# Windows: winget install pandoc
# Mac: brew install pandoc
```

5. Salvar em local indicado pelo usuário

## Estrutura padrão por tipo

**Deck de vendas:**
- Capa
- O problema do cliente
- A solução
- Como funciona
- Resultados / prova social
- Investimento
- Próximos passos

**Apresentação de projeto:**
- Capa
- Contexto / objetivo
- O que foi feito
- Resultados
- Próximos passos

**Treinamento:**
- Capa
- Agenda
- Módulos de conteúdo (1 conceito por slide)
- Exercício / prática
- Resumo e encerramento

## Regras de design

- Máximo 5 linhas de texto por slide
- 1 ideia central por slide
- Título curto e direto
- Se tiver design guide, aplicar as cores e fontes
- Salvar em `projetos/[nome]/` ou onde o usuário indicar
