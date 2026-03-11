---
name: cclhm0076-docencia
description: >
  Use esta skill para qualquer tarefa no repositório da disciplina CCLHM0076 —
  História da América: colonização e resistência (UNILAB, Eric Brasil). Acione sempre
  que o trabalho envolver: criar ou editar arquivos .qmd (Quarto/RevealJS), produzir
  fichamentos ou sínteses bibliográficas, elaborar atividades pedagógicas, montar ou
  revisar cronogramas, commitar alterações no branch 2026_1, ou preencher templates
  da pasta templates-quarto/. Nunca inventar conteúdo histórico, bibliográfico ou
  atribuído a autores. Qualquer tarefa ligada à disciplina, ao repositório ou aos seus
  materiais deve acionar esta skill.
---

# SKILL — cclhm0076-docencia

## Contexto do projeto

Repositório de materiais da disciplina **CCLHM0076 — História da América: colonização
e resistência**, ministrada por **Eric Brasil** no curso de Licenciatura em História
do Instituto de Humanidades e Letras da **UNILAB**.

**Site publicado:** `https://ericbrasil.com.br/cclhm0076/`

**URLs relevantes:**

| Recurso | URL |
|---|---|
| Página principal | `https://ericbrasil.com.br/cclhm0076/` |
| Ementa HTML | `https://ericbrasil.com.br/cclhm0076/ementa/ementa` |
| Ementa PDF | `https://ericbrasil.com.br/cclhm0076/ementa/ementa.pdf` |
| Calendário HTML | `https://ericbrasil.com.br/cclhm0076/ementa/calendario` |
| Calendário PDF | `https://ericbrasil.com.br/cclhm0076/ementa/calendario.pdf` |
| Slides aula N | `https://ericbrasil.com.br/cclhm0076/slides/aula-N/` |

**Estrutura do repositório:**

```
cclhm0076/                         ← raiz do repositório
├── .claude/
│   └── CLAUDE.md
├── bibliografia/
├── cclhm0076-docencia/            ← subpasta da skill
│   ├── templates-quarto/
│   │   ├── template-html.qmd
│   │   ├── template-pdf.qmd
│   │   └── template-slides.qmd
│   └── SKILL.md
├── ementa/
│   ├── calendario_files/libs/
│   ├── ementa_files/libs/
│   ├── calendario.html
│   ├── calendario.md
│   ├── calendario.pdf
│   ├── ementa.html
│   ├── ementa.md
│   └── ementa.pdf
├── imgs/
├── index_files/
├── slides/
│   ├── aula-1/ … aula-15/        ← apresentações (ementa prevê até aula-16)
│   │   ├── index.qmd
│   │   ├── index.html
│   │   └── index_files/
│   ├── imgs/                      ← imagens e QR codes compartilhados
│   ├── custom.scss
│   └── slides_old/                ← HTML legado para consulta/conversão
├── tarefas/
├── index.html
├── index.md
├── LICENSE.md
└── README.md
```

**Branch de trabalho ativo:** `2026_1`
**Branch consolidado:** `main` — nunca commitar diretamente.

---

## Bootstrap — início obrigatório de sessão

Ao iniciar qualquer tarefa neste repositório, executar **antes de qualquer alteração**:

```bash
git branch --show-current      # confirmar que está em 2026_1
git status                     # verificar estado atual
git log --oneline -5           # entender o histórico recente
```

Se não estiver no branch correto:

```bash
git checkout 2026_1
```

Ler sempre para contextualizar a sessão:

- `ementa/ementa.md` — objetivos, avaliação, conteúdo programático
- `ementa/calendario.md` — datas e temas de todas as aulas

---

## Princípios inegociáveis

### 1. Nunca inventar conteúdo

Proibido produzir:

- informações históricas sem base textual
- argumentos ou interpretações atribuídos a autores sem o texto em mãos
- citações — mesmo paráfrases devem ter o texto como fonte
- referências bibliográficas não fornecidas pelo docente
- datas, dados ou exemplos por suposição

**Quando o texto não estiver disponível no contexto**, não simular leitura. Agir assim:

1. Informar: *"O texto [título] não foi fornecido. Para prosseguir, cole o conteúdo
   ou indique o caminho do arquivo no repositório."*
2. Oferecer o que pode ser feito com o material disponível.
3. Jamais preencher lacunas com inferências não declaradas.

### 2. Usar sempre a bibliografia indicada como base

- Partir da bibliografia da disciplina e dos textos fornecidos no repositório.
- Não inserir referências externas por iniciativa própria.
- Sugerir leituras adicionais **somente se solicitado explicitamente**.

### 3. Tom acadêmico de graduação em História

Escrever de forma: clara, formal, analítica, historicamente rigorosa.

Evitar: linguagem coloquial, simplificações indevidas, jargão desnecessário,
tom genérico, afirmações categóricas sem base, voz de assistente virtual.

---

## Produção de conteúdo

### Fichamentos e sínteses bibliográficas

Ao trabalhar com textos fornecidos, identificar quando possível:

- tema central e argumento principal
- conceitos-chave utilizados pelo autor
- recorte temporal e espacial
- fontes ou abordagem metodológica
- relevância para os debates da disciplina

O texto produzido deve ser útil para estudo, preparação de aula e debate em sala,
sem extrapolar o que o autor sustenta.

### Atividades pedagógicas

Estrutura mínima para toda atividade elaborada:

| Campo | Conteúdo |
|---|---|
| **Objetivo** | O que se espera que o estudante desenvolva |
| **Descrição** | O que será feito, em que formato |
| **Materiais** | Textos, fontes ou recursos necessários |
| **Orientações** | Como realizar a atividade |
| **Avaliação** | Critérios básicos de acompanhamento |

As atividades devem estar ancoradas na bibliografia da disciplina e estimular leitura,
reflexão, debate e análise histórica compatíveis com o nível de graduação.

---

## Diretrizes para arquivos Quarto (.qmd)

### Templates disponíveis

A pasta `templates-quarto/` contém os modelos base do projeto:

| Arquivo | Finalidade |
|---|---|
| `template-slides.qmd` | Apresentações RevealJS |
| `template-html.qmd` | Páginas e materiais HTML |
| `template-pdf.qmd` | Documentos para exportação PDF |

**Ao criar novos materiais:** sempre partir do template correspondente.

**Se os templates estiverem desatualizados:** ler os `index.qmd` existentes em
`slides/aula-N/` para confirmar o padrão de YAML e estrutura em uso.

### YAML frontmatter padrão — slides

```yaml
---
title: "Aula N: Título da aula"
date: "AAAA-MM-DD"
date-format: full
lang: pt-br
format:
  revealjs:
    theme: [default, ../custom.scss]
    slide-number: true
    incremental: false
    chalkboard:
      buttons: true
    footer: "Eric Brasil | <a href=https://ericbrasil.com.br/contact/>Entre em contato</a> | CCLHM0076 — História da América: colonização e resistência"
    logo: https://raw.githubusercontent.com/ericbrasiln/cclhm0081/63cc875c152f361a14f723efbe6bd161f5aaf8b6/banner_logos_hist.png
author:
  - name: Eric Brasil
    orcid: 0000-0001-5067-8475
toc: false
---
```

Campos **ausentes** intencionalmente: `subtitle`, `email`, `affiliation`.

### Convenções de slides RevealJS

| Elemento | Sintaxe |
|---|---|
| Separador | `---` |
| Slide com título | `## Título {.center}` |
| Slide sem título | `## {.center}` |
| Background image + conteúdo | `## Título {background-image="url" background-opacity="0.X" .center}` |
| Background image full | `## {background-image="url"}` |
| Background iframe | `## {background-iframe="url" background-interactive="true"}` |
| Overlay em iframe | `::: {style="position: absolute; width: 40%; right: 0; ..."}` |
| Imagem simples | `![Legenda](url){width=X%}` |
| Imagem com link na legenda | `![[Texto do link](url-fonte)](url-imagem){width=X%}` |
| Citação | `>` blockquote + `(AUTOR, data, p. N)` na linha seguinte |
| Lista | `- item` (sem `*`) |

### Estrutura obrigatória de toda apresentação

1. **Primeiro slide:** QR code de acesso — `![Acesse a apresentação](../imgs/qrc_aulaN.png)`
2. **Conteúdo:** slides temáticos seguindo a ementa
3. **Último slide:** `## Bibliografia da aula {.center}` com lista das leituras obrigatórias

### Citações

Formato padrão em slides: `(AUTOR, data, p. N)`

Exemplo no blockquote:
```
> "Trecho da citação."

(SANTOS, 2014, p. 221)
```

Na bibliografia final, usar formato ABNT completo.

### QR codes

Gerar com `qrencode` para cada nova apresentação:

```bash
qrencode -o slides/imgs/qrc_aulaN.png -s 10 -m 2 "https://ericbrasil.com.br/cclhm0076/slides/aula-N/"
```

Commitar a imagem separadamente, antes dos slides:
```
[Claude Code] feat: adiciona QR code para slides da aula N
```

### Conversão de HTML legado (`slides_old/`)

Ao converter slides de `slides_old/index.html`:

1. Ler o trecho solicitado (linhas indicadas pelo docente)
2. Verificar imagens locais (`img/`) → confirmar existência em `slides/imgs/`
3. Converter para QMD seguindo `template-slides.qmd`
4. Manter conteúdo fiel ao original; não resumir nem acrescentar sem autorização
5. Atualizar referências bibliográficas conforme a ementa da aula correspondente
6. O docente renderiza com `quarto render`; só então commitar

### Ao criar ou editar .qmd

- Reaproveitar o YAML, seções e padrões de organização já adotados no projeto
- Preservar o estilo do docente — evitar mudanças que descaracterizem o material
- Evitar excesso de texto por slide: favorecer exposição oral, leitura e debate
- Organizar conceitos e exemplos de forma progressiva e compreensível

---

## Fluxo de trabalho com Git

### Procedimento padrão

```
editar/criar arquivos
    → docente renderiza com quarto
    → Claude Code commita atomicamente
    → git push origin 2026_1
    → abrir PR de 2026_1 → main via gh pr create
```

### Commits

```bash
git status                  # verificar arquivos modificados
git diff                    # revisar o que mudou antes de commitar
git add <arquivos>          # nunca usar git add . sem revisar
git commit -m "[Claude Code] tipo: descrição breve

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>"
```

Nunca usar `git push --force`. Nunca commitar diretamente em `main`.

### Padrão de commits

| Tipo | Uso |
|---|---|
| `feat` | novo material ou arquivo criado |
| `fix` | correção de erro em arquivo existente |
| `docs` | atualização de documentação ou síntese |
| `refactor` | reorganização sem mudança de conteúdo |
| `chore` | ajustes técnicos, YAML, metadados |

### Commits atômicos

Cada commit deve conter uma mudança pequena, coerente e identificável. Exemplos:

```
[Claude Code] feat: adiciona QR code para slides da aula 3
[Claude Code] feat: adiciona slides da aula 3 — Sociedades autóctones
[Claude Code] refactor: atualiza template-slides.qmd
[Claude Code] fix: corrige link para ementa.pdf no index.md
```

Não misturar: criação de slides + atualização de template + edição de ementa no mesmo commit.

### Pull Requests

Todo push para `2026_1` deve ser seguido de PR para `main` via `gh pr create`.

O corpo do PR deve:
- Descrever as alterações por arquivo/seção
- Incluir tabela de commits quando houver mais de um
- Deixar explícito que foi criado pelo Claude Code
- Encerrar com `🤖 Criado com [Claude Code](https://claude.com/claude-code)`

---

## Convenções editoriais

- **Nomes de arquivo:** minúsculas com hífens — ex.: `aula-03-colonialismo.qmd`
- **Organização:** por aula ou unidade temática, não por tipo de arquivo
- **Antes de criar:** verificar se o conteúdo já existe no repositório
- **Antes de commitar:** revisar ortografia, gramática e coerência
- **Preservar:** comentários, metadados e estruturas YAML relevantes já existentes
- **Voz dos textos:** refletir o docente, não uma redação genérica de assistente

---

## Limites de atuação

Esta skill não deve:

- alterar a organização do repositório sem solicitação ou justificativa clara
- apagar conteúdo sem confirmação do docente
- substituir a voz docente por redação genérica
- inserir bibliografia, interpretações ou dados sem base nos materiais fornecidos
- simular leitura de textos não fornecidos no contexto

**Quando houver dúvida, a prioridade é:**

1. Preservar o que já existe
2. Trabalhar com o material efetivamente disponível
3. Explicitar limites em vez de improvisar conteúdo
