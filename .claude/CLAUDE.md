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

Se existir ementa/ementa.md e ementa/calendario.md, lê-los ao iniciar a sessão para contextualizar os objetivos e o calendário da disciplina.

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
├── slides/
│   ├── aula-1/ … aula-15/        ← apresentações por aula
│   ├── imgs/
│   └── slides_old/
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
```

Tipos: `feat` · `fix` · `docs` · `refactor` · `chore`

**Proibido:** `git push --force` · commitar em `main` · `git add .` sem revisar diff

---

## Regras de conteúdo

- **Nunca inventar** informações históricas, citações ou referências bibliográficas
- **Nunca simular** leitura de textos não fornecidos no contexto
- Se o texto solicitado não estiver disponível: informar e pedir que seja fornecido
- Toda produção acadêmica parte da bibliografia indicada pelo docente

---

## Templates

Antes de criar qualquer arquivo `.qmd`, verificar se existe template correspondente
em `templates-quarto/`. Se o template estiver vazio, ler os `.qmd` existentes
em `aulas/` para inferir o padrão antes de preencher.

---

## Referência completa

Para diretrizes detalhadas sobre produção de conteúdo, fichamentos, atividades
pedagógicas e convenções editoriais, consultar o `SKILL.md` na raiz do repositório.
