---
name: yt-transcript
description: >
  Extrai transcrição de vídeos do YouTube usando yt-dlp.
  Suporta múltiplos idiomas. Use para criar conteúdo a partir de vídeos:
  carrosseis, newsletters, posts, roteiros.
---

# /yt-transcript — Extrair Transcrição de Vídeo do YouTube

## Dependência

Requer `yt-dlp` instalado. Verificar antes de rodar:

```bash
yt-dlp --version
```

Se não estiver instalado:
- **Windows:** `winget install yt-dlp` ou baixar em yt-dlp.github.io
- **Mac:** `brew install yt-dlp`

---

## Input

O usuário fornece a URL do vídeo do YouTube.

---

## Workflow

### 1. Verificar yt-dlp

```bash
yt-dlp --version
```

Se não encontrado, informar como instalar e parar.

### 2. Extrair transcrição

```bash
yt-dlp --write-auto-sub --sub-lang pt,en --skip-download --output "%(title)s" [URL]
```

Se não houver legenda automática disponível em português, tentar inglês e informar o usuário.

### 3. Converter para texto limpo

Após extrair o arquivo `.vtt` ou `.srt`, limpar o conteúdo:
- Remover timestamps
- Remover marcações de formatação
- Juntar linhas quebradas em parágrafos naturais

### 4. Salvar

Salvar a transcrição limpa em `dados/transcricao-[título-do-vídeo].md`

### 5. Perguntar o que fazer com o conteúdo

> "Transcrição extraída e salva. O que você quer fazer com ela?
>
> - Criar um carrossel → `/carrossel`
> - Criar uma newsletter → `/roteiro-post`
> - Resumir os pontos principais → peço um resumo agora
> - Usar como input pro Waterfall → você decide como aproveitar"

---

## Regras

- Se o vídeo não tiver legendas automáticas, informar claramente e sugerir alternativas (ex: transcrever manualmente e colar o texto)
- Não modificar o conteúdo da transcrição além da limpeza de formatação
- Sempre salvar em `dados/` antes de processar
