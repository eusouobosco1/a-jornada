---
name: pdf
description: >
  Manipula PDFs: extrai texto e tabelas, analisa conteúdo, cria resumos.
  Use para extrair dados de contratos, analisar documentos, criar resumos executivos.
---

# /pdf — Trabalhar com PDFs

## Input

O usuário fornece:
- Caminho do arquivo PDF (ou coloca na pasta `dados/`)
- O que quer fazer com ele

## O que pode fazer

### Extrair e analisar
- Ler o conteúdo completo do PDF
- Extrair trechos específicos (por tema, seção, palavra-chave)
- Resumir o documento em pontos principais
- Comparar dois PDFs

### Criar resumos
- Resumo executivo (1 página)
- Bullet points dos pontos principais
- Timeline de eventos (se for contrato ou processo)
- Tabela de dados extraídos

### Analisar contratos e documentos formais
- Identificar cláusulas importantes
- Destacar riscos ou pontos de atenção
- Comparar com versão anterior

## Workflow

1. Ler o arquivo com a ferramenta de leitura
2. Confirmar o que foi entendido do documento em 2-3 linhas
3. Executar a tarefa solicitada
4. Salvar o output em `dados/[nome-do-arquivo]-resultado.md` se for um resumo ou análise

## Regras

- Nunca modificar o PDF original
- Se o PDF tiver imagens sem texto (PDF escaneado), informar que não é possível extrair o texto diretamente
- Sempre confirmar o que foi entendido antes de analisar documentos longos
