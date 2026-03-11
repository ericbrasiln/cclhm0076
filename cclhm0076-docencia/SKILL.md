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

**Estrutura esperada do repositório:**

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
│   ├── aula-1/ … aula-15/        ← 15 aulas individuais
│   ├── imgs/
│   └── slides_old/
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
ls -la                         # mapear estrutura raiz
```

Se não estiver no branch correto:

```bash
git checkout 2026_1
```

Se a pasta `aulas/` ou `bibliografia/` existir, listá-la também para mapear o
material disponível antes de qualquer produção de conteúdo.

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

**Ao criar novos materiais:** sempre partir do template correspondente, nunca de zero
ou de modelos externos.

**Se os templates estiverem vazios:** ler os arquivos `.qmd` existentes no repositório
para inferir o padrão de YAML e estrutura antes de preencher qualquer template.

### Ao criar ou editar .qmd

- Reaproveitar o YAML, seções e padrões de organização já adotados no projeto
- Preservar o estilo do docente — evitar mudanças que descaracterizem o material
- Evitar excesso de texto por slide: favorecer exposição oral, leitura e debate
- Organizar conceitos e exemplos de forma progressiva e compreensível

---

## Fluxo de trabalho com Git

### Procedimento pré-alteração

```bash
git branch --show-current   # deve retornar: 2026_1
git status                  # verificar arquivos modificados
```

### Procedimento pós-alteração

```bash
git diff                    # revisar o que mudou antes de commitar
git add <arquivos>          # nunca usar git add . sem revisar
git commit -m "[Claude Code] tipo: descrição breve"
```

Nunca usar `git push --force`. Nunca fazer merge em `main` sem instrução explícita
do docente.

### Padrão de commits

Todo commit feito pelo Claude Code deve seguir:

```
[Claude Code] tipo: descrição breve da alteração
```

Tipos válidos (convencional commits):

| Tipo | Uso |
|---|---|
| `feat` | novo material ou arquivo criado |
| `fix` | correção de erro em arquivo existente |
| `docs` | atualização de documentação ou síntese |
| `refactor` | reorganização sem mudança de conteúdo |
| `chore` | ajustes técnicos, YAML, metadados |

**Exemplos:**

```
[Claude Code] feat: cria template base para slides em Quarto
[Claude Code] fix: corrige YAML da aula 03
[Claude Code] docs: adiciona fichamento do texto de Quijano (unidade 1)
[Claude Code] chore: reorganiza cronograma do semestre 2026.1
```

### Commits atômicos

Cada commit deve conter uma mudança pequena, coerente e identificável. Não misturar:
revisões textuais + criação de templates + reorganização estrutural no mesmo commit.

---

## Convenções editoriais

- **Nomes de arquivo:** minúsculas com hífens — ex.: `aula-01-colonialismo.qmd`,
  `ficha-quijano-2000.md`
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
