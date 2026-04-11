---
name: xlsx
description: >
  Cria e edita planilhas Excel (.xlsx) com fórmulas, formatação e análise de dados.
  Use para relatórios financeiros, dashboards, controle de metas, análise de dados.
---

# /xlsx — Criar Planilha Excel

## Input

O usuário fornece:
- O que precisa controlar ou analisar
- Dados brutos (se tiver) ou estrutura desejada

## Workflow

1. Entender o objetivo da planilha
2. Propor a estrutura (colunas, abas, fórmulas) antes de criar
3. Criar o arquivo usando openpyxl (Python) ou gerar CSV estruturado:

```bash
# Verificar Python disponível
python --version

# Instalar openpyxl se necessário
pip install openpyxl
```

4. Se Python não estiver disponível, gerar como CSV e instruir como abrir no Excel
5. Salvar em local indicado pelo usuário

## Tipos comuns

**Controle financeiro:**
- Receitas e despesas por categoria
- Saldo acumulado
- Gráfico de evolução

**Controle de metas:**
- Meta vs. realizado
- Percentual de atingimento
- Tendência

**Pipeline / CRM simples:**
- Nome do lead
- Status (contato, proposta, fechado, perdido)
- Valor
- Data

**Calendário de conteúdo:**
- Data, canal, tema, status, link

## Regras

- Sempre mostrar a estrutura proposta antes de criar
- Fórmulas documentadas com comentário quando não forem óbvias
- Salvar em `dados/` ou onde o usuário indicar
- Se os dados forem sensíveis (financeiro), lembrar de não commitar em repositório público
