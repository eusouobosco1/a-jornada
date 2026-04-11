---
name: frontend-design
description: >
  Cria interfaces web completas com design de alta qualidade.
  Gera HTML/CSS pronto pra usar, com visual profissional.
  Use para landing pages, dashboards, páginas de produto, componentes web.
---

# /frontend-design — Criação de Interface Web

## Input

O usuário descreve o que precisa. Pode ser:
- Tipo de página (landing page, dashboard, formulário, portfólio)
- Referência visual (link, descrição, print)
- Conteúdo a incluir (textos, seções, funcionalidades)
- Identidade visual (se tiver `marca/design-guide.md`, ler antes de começar)

---

## Workflow

### 1. Entender o objetivo

Antes de criar, confirmar:
- Qual é o propósito da página? (converter, informar, capturar lead, apresentar)
- Quem vai ver? (cliente, equipe interna, público geral)
- Tem identidade visual definida? (verificar `marca/design-guide.md` se existir)
- Precisa funcionar em mobile? (padrão: sim)

### 2. Criar o HTML

Gerar arquivo HTML completo com CSS inline ou em `<style>`:
- Sem dependências externas além de Google Fonts (se necessário)
- Responsivo por padrão (mobile-first)
- Comentários nos blocos principais para facilitar edição
- Visual que foge da estética genérica de IA — atenção a espaçamento, tipografia e hierarquia

**Princípios visuais:**
- Hierarquia clara: o olho sabe onde ir primeiro
- Espaçamento generoso — páginas apertadas parecem amadores
- Máximo 2 fontes
- Contraste suficiente para leitura
- CTA visível sem rolar a página

### 3. Salvar e testar

Salvar em local indicado pelo usuário ou em `projetos/[nome]/index.html`.

Abrir no browser para verificar:
```bash
start [caminho/para/arquivo.html]
```

### 4. Checkpoint

Mostrar o resultado e perguntar:
- O que mudar no visual?
- Falta alguma seção?
- Quer versão mobile revisada?

### 5. Ajustar conforme feedback

Editar diretamente o arquivo. Não recriar do zero a não ser que o usuário peça.

---

## Output

Arquivo HTML completo, pronto pra abrir no browser ou publicar com `/publicar-site`.

## Regras

- Sempre ler `marca/design-guide.md` antes de criar qualquer visual, se existir
- Não usar frameworks externos (Bootstrap, Tailwind via CDN) sem o usuário pedir — gera dependência
- Código limpo e comentado para facilitar edição futura
- Se o usuário pedir React ou outro framework, criar o projeto estruturado corretamente
