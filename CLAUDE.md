# A Jornada — Claude Code OS

## O que é esse workspace

Workspace da marca pessoal de Bosco (@eusouobosco). Aqui ele produz conteúdo, opera o sistema Waterfall e toca a estratégia da Jornada.

**Estrutura de pastas:**
- `_contexto/` — memória do sistema (não apagar)
- `conteudo/` — produção por tipo (carrosseis, newsletters, roteiros)
- `projetos/` — projetos internos da Jornada
- `marca/` — identidade visual e design guide
- `dados/` — arquivos pra análise (CSV, PDF, etc)
- `templates/skills/` — templates de skills prontos pra personalizar com /mapear
- `templates/ferramentas/catalogo.md` — APIs e ferramentas disponíveis pra usar em skills
- `tarefas.md` — lista de tarefas corrente

## Sobre o negócio

Bosco é João Bosco Monteiro, criador de conteúdo sobre desenvolvimento masculino, fé, família e empreendedorismo. A marca é @eusouobosco, o projeto central é "A Jornada". Trabalha com ~2h/dia enquanto está no CLT (Rillsoft). A esposa Maysa (@maysamontei) é parceira no Montei Studio, projeto separado.

## O que mais fazemos aqui

- Rodar o sistema Waterfall: transcrição bruta → YouTube, Substack, LinkedIn, Instagram
- Criar carrosseis e visuais com o design system (fundo `#0C0C0C`, accent `#C9A053`, Poppins 800)
- Planejar e organizar a estratégia de conteúdo da Jornada
- Desenvolver e iterar os agentes do Opensquat (squad waterfall-jornada)

## Público

Homens jovens (~22 anos) e maduros (~34-35 anos) que buscam um irmão mais velho que já deu alguns passos — sobre vida, família, fé e empreendedorismo.

## Tom de voz

Irmão mais velho. Direto, "Pá-Pum". Confrontacional com propósito, acolhedor na forma. Real e vulnerável. Frases curtas, sem enrolação.

Nunca: coach genérico, autoajuda vazia, superlativos inflados, Red Pill agressivo, espiritualidade new age, motivacional vazio.

## Posicionamento

"A jornada é o que importa." — frase de encerramento obrigatória em todo conteúdo.
Documenta a própria jornada. Não é guru — é quem está no caminho e compartilha o que aprendeu.

## Ferramentas conectadas

- [x] Claude Code
- [x] Opensquat (squad waterfall-jornada operacional)
- [ ] Playwright MCP (necessário pra renderizar PNGs dos slides)
- [ ] Google Calendar

---

## Contexto do negócio

No início de toda conversa, ler os seguintes arquivos (se existirem e estiverem configurados):

1. `_contexto/empresa.md` — quem é o usuário, o que faz, como funciona o negócio
2. `_contexto/preferencias.md` — tom de voz, estilo de escrita, o que evitar
3. `_contexto/estrategia.md` — foco atual, prioridades, o que pode esperar

Usar essas informações como base pra qualquer resposta ou decisão. Ao sugerir prioridades, formatos ou abordagens, considerar o foco atual descrito em `estrategia.md`.

Para qualquer tarefa visual (carrossel, proposta, slide, landing page), consultar `marca/design-guide.md` como referência de estilo.

Não é necessário listar o que foi lido nem confirmar a leitura. Apenas usar o contexto naturalmente.

---

## Fluxo de trabalho

Antes de executar qualquer tarefa, verificar se existe uma skill relevante em `.claude/skills/` ou `.claude/commands/`.
Se encontrar, seguir as instruções da skill.
Se não encontrar, executar a tarefa normalmente.

Ao concluir uma tarefa que não tinha skill mas parece repetível (o usuário provavelmente vai pedir de novo no futuro), perguntar:

> "Isso pode virar uma skill pra próxima vez. Quer que eu crie?"

Não perguntar pra tarefas pontuais ou perguntas simples. Só quando o padrão de repetição for claro.

---

## Aprender com correções

Quando o usuário corrigir algo, melhorar uma resposta ou dar uma instrução que parece permanente (frases como "na verdade é assim", "não faça mais isso", "prefiro assim", "sempre que...", "evita...", "da próxima vez..."), perguntar:

> "Quer que eu salve isso pra não precisar repetir?"

Se sim, identificar onde faz mais sentido salvar:

- **Sobre o negócio** (quem são os clientes, como funciona a empresa, serviços, mercado) → adicionar em `_contexto/empresa.md`
- **Sobre preferências e estilo** (tom de voz, formato de resposta, o que evitar, como estruturar textos) → adicionar em `_contexto/preferencias.md`
- **Sobre prioridades e foco atual** (projetos em andamento, metas do momento, prazos importantes, o que é prioridade agora) → adicionar em `_contexto/estrategia.md`
- **Regra de comportamento nessa pasta** (onde salvar arquivos, como nomear, fluxos específicos) → adicionar no próprio `CLAUDE.md`

Salvar com uma linha nova clara, sem reformatar o arquivo inteiro. Confirmar o que foi salvo mostrando a linha adicionada.

Não perguntar se a correção for óbvia de contexto imediato (ex: "na verdade o arquivo se chama X"). Só perguntar quando a informação tiver valor duradouro.

---

## Manter contexto atualizado

Ao terminar uma tarefa que mudou algo relevante no projeto (novo cliente, nova skill, mudança de foco, novo processo, ferramenta instalada, estrutura de pastas alterada), perguntar:

> "Isso mudou algo no teu contexto. Quer que eu atualize os arquivos de memória?"

Se sim, identificar o que precisa atualizar:

- **Novo cliente, serviço, ferramenta, equipe** → `_contexto/empresa.md`
- **Mudança de prioridade ou foco** → `_contexto/estrategia.md`
- **Correção de tom ou estilo** → `_contexto/preferencias.md`
- **Nova pasta, regra de organização, skill criada** → `CLAUDE.md`
- **Mudança visual (cores, fontes, logo)** → `marca/design-guide.md`

Mostrar o que vai mudar antes de salvar. Não reformatar o arquivo inteiro, só adicionar ou editar a linha relevante.

**Quando NÃO perguntar:**
- Tarefas pontuais que não mudam o contexto (ex: escrever um email, criar um post avulso)
- Perguntas simples ou conversas sem ação
- Mudanças que já foram salvas pelo bloco "Aprender com correções"

**Dica:** se não sabe se algo mudou, rode `/atualizar` pra uma varredura completa.

---

## Criação de skills

Quando o usuário pedir pra criar uma nova skill:

1. Verificar se existe um template relevante em `templates/skills/`. Se existir, usar como base e adaptar pro contexto do usuário
2. Perguntar: "Essa skill é específica pra esse projeto ou vai ser útil em qualquer projeto?"
   - Específica desse negócio → salvar em `.claude/skills/nome-da-skill/SKILL.md` (local)
   - Útil em qualquer projeto → salvar em `~/.claude/skills/nome-da-skill/SKILL.md` (global)
3. Ler `_contexto/empresa.md` e `_contexto/preferencias.md` pra calibrar o conteúdo da skill ao contexto do negócio
4. Se a skill precisar de arquivos de apoio (templates, referências, exemplos), criar dentro da pasta da skill
5. Seguir o fluxo da skill-creator nativa do Claude Code
