# CLAUDE.md — cclhm0076-docencia

Instruções operacionais para o Claude Code neste repositório.

> Este arquivo complementa o `SKILL.md` da skill `cclhm0076-docencia`.
> O SKILL.md contém os princípios e diretrizes completas.
> Este arquivo contém os comportamentos automáticos e atalhos de sessão.

---

## Identidade do projeto

| Campo | Valor |
|---|---|
| Disciplina | CCLHM0076 — História da América: colonização e resistência |
| Docente | Eric Brasil |
| Curso | Licenciatura em História |
| Instituição | Instituto de Humanidades e Letras — UNILAB |
| Semestre ativo | 2026.1 |
| Branch de trabalho | `2026_1` |
| Branch consolidado | `main` |
| Site publicado | `https://ericbrasil.com.br/cclhm0076/` |

---

## Ao iniciar qualquer sessão

Executar automaticamente, sem precisar ser solicitado:

```bash
git branch --show-current
git status
git log --oneline -5
```

Se o branch atual não for `2026_1`:

```bash
git checkout 2026_1
```

Ler sempre ao iniciar, para contextualizar objetivos e calendário:

- `ementa/ementa.md`
- `ementa/calendario.md`

---

## Estrutura do repositório

```
cclhm0076/                         ← raiz do repositório
├── .claude/
│   └── CLAUDE.md                  ← este arquivo
├── bibliografia/
├── cclhm0076-docencia/            ← subpasta da skill
│   ├── templates-quarto/
│   │   ├── template-html.qmd
│   │   ├── template-pdf.qmd
│   │   └── template-slides.qmd
│   └── SKILL.md                   ← princípios e diretrizes completas
├── ementa/
│   ├── calendario.md / .html / .pdf
│   └── ementa.md / .html / .pdf
├── imgs/
├── index_files/
├── slides/
│   ├── aula-1/ … aula-15/        ← apresentações por aula (ementa prevê até aula-16)
│   │   ├── index.qmd              ← fonte Quarto
│   │   ├── index.html             ← renderizado
│   │   └── index_files/           ← assets do RevealJS
│   ├── imgs/                      ← imagens e QR codes compartilhados
│   ├── custom.scss                ← tema visual das apresentações
│   └── slides_old/                ← HTML legado para consulta/conversão
├── tarefas/
├── index.html
├── index.md
└── README.md
```

---

## Regras de commit

Todo commit neste repositório deve:

1. Estar no branch `2026_1`
2. Ser atômico (uma mudança por commit)
3. Seguir o padrão:

```
[Claude Code] tipo: descrição breve

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
```

Tipos: `feat` · `fix` · `docs` · `refactor` · `chore`

**Proibido:** `git push --force` · commitar em `main` · `git add .` sem revisar diff

---

## Fluxo padrão de trabalho

```
editar/criar arquivos
    → renderizar com quarto (feito pelo docente)
    → commitar atomicamente (Claude Code)
    → git push origin 2026_1
    → abrir PR de 2026_1 → main via gh pr create
```

O PR deve:
- Ter título descritivo e conciso
- Ter corpo detalhando as alterações por arquivo/seção
- Deixar explícito que foi criado pelo Claude Code
- Incluir `🤖 Criado com [Claude Code](https://claude.com/claude-code)` no rodapé

---

## Slides RevealJS — padrões operacionais

### YAML frontmatter obrigatório

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

### Convenções de slides

- Separador entre slides: `---`
- Título de slide: `## Título {.center}`
- Citações: `>` blockquote + autor na linha seguinte no formato `(AUTOR, data, p. N)`
- Imagens com fonte: `![[Legenda](url-fonte)](url-imagem){width=X%}`
- Background de imagem: `## Título {background-image="url" background-opacity="0.X" .center}`
- Background de iframe: `## {background-iframe="url" background-interactive="true"}`
- Overlay em iframe: `::: {style="position: absolute; width: 40%; right: 0; ..."}`
- Primeiro slide: QR code de acesso (`../imgs/qrc_aulaN.png`)
- Último slide: bibliografia com leituras obrigatórias da aula

### QR codes

Gerar com `qrencode` para cada apresentação nova:

```bash
qrencode -o slides/imgs/qrc_aulaN.png -s 10 -m 2 "https://ericbrasil.com.br/cclhm0076/slides/aula-N/"
```

Salvar em `slides/imgs/` com o padrão `qrc_aulaN.png`.
Inserir como primeiro slide: `![Acesse a apresentação](../imgs/qrc_aulaN.png)`

### Conversão de HTML legado

Ao converter slides de `slides_old/index.html`:

1. Ler o trecho solicitado (linhas indicadas pelo docente)
2. Confirmar imagens locais referenciadas (`img/`) → verificar se existem em `slides/imgs/`
3. Converter seguindo o template em `templates-quarto/template-slides.qmd`
4. Manter conteúdo fiel ao original — não inventar, não resumir sem autorização
5. Atualizar referências bibliográficas conforme ementa da aula correspondente

---

## Regras de conteúdo

- **Nunca inventar** informações históricas, citações ou referências bibliográficas
- **Nunca simular** leitura de textos não fornecidos no contexto
- Se o texto solicitado não estiver disponível: informar e pedir que seja fornecido
- Toda produção acadêmica parte da bibliografia indicada pelo docente

---

## Templates

Antes de criar qualquer arquivo `.qmd`, verificar se existe template correspondente
em `cclhm0076-docencia/templates-quarto/`. Se o template estiver vazio, ler os
`.qmd` existentes em `slides/aula-N/` para inferir o padrão antes de preencher.

---

## Referência completa

Para diretrizes detalhadas sobre produção de conteúdo, fichamentos, atividades
pedagógicas e convenções editoriais, consultar `cclhm0076-docencia/SKILL.md`.
