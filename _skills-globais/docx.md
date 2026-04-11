---
name: docx
description: >
  Cria e edita documentos Word (.docx) com formatação profissional.
  Use para propostas formais, contratos, documentos para clientes que pedem Word.
---

# /docx — Criar Documento Word

## Input

O usuário fornece:
- Tipo de documento (proposta, contrato, relatório, carta, etc.)
- Conteúdo ou briefing

## Workflow

1. Entender o tipo e propósito do documento
2. Criar o conteúdo completo em markdown bem estruturado
3. Converter para .docx usando pandoc:

```bash
pandoc input.md -o output.docx --reference-doc=template.docx
```

Se pandoc não estiver instalado:
- **Windows:** `winget install pandoc`
- **Mac:** `brew install pandoc`

Se não tiver template de referência, gerar com formatação padrão limpa.

4. Salvar em local indicado pelo usuário

## Estrutura padrão por tipo

**Proposta:**
- Capa (nome do cliente, data, nome do serviço)
- Sobre nós (breve)
- Entendimento do problema
- Solução proposta
- Escopo e entregáveis
- Investimento
- Próximos passos

**Relatório:**
- Sumário executivo
- Contexto
- Análise / dados
- Conclusões
- Recomendações

**Carta formal:**
- Cabeçalho
- Corpo
- Encerramento

## Regras

- Sempre salvar em `projetos/[nome]/` ou onde o usuário indicar
- Se o usuário tiver template Word próprio, pedir o arquivo antes de gerar
- Linguagem formal mas não burocrática — clara e direta
