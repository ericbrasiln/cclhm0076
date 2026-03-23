# questoes-apoio.md — Questões de leitura guiada

Referência para elaboração de questões de apoio à leitura dos estudantes.
As questões acompanham o texto enviado e funcionam como roteiro de leitura guiada.

---

## Quando usar este arquivo

Ler este arquivo antes de qualquer tarefa que envolva elaborar questões de apoio
à leitura para um texto da bibliografia da disciplina.

**Pré-requisito inegociável:** o texto deve estar disponível no contexto. As
questões devem ser respondíveis a partir do próprio texto — nunca exigir
conhecimento externo não fornecido aos estudantes.

---

## Número de questões

Entre **5 e 8 questões**. Nem menos que 5, nem mais que 8.

O número exato depende da extensão e complexidade do texto. Textos mais longos
ou com múltiplos tópicos admitem até 8; textos mais curtos ou focados pedem
entre 5 e 6.

---

## Dimensões a cobrir

As questões devem, em conjunto, cobrir as seguintes dimensões — sem necessidade
de ordem fixa nem de uma questão por dimensão:

| Dimensão | O que explorar |
|---|---|
| **Problema e objetivos** | O que o texto busca responder ou demonstrar |
| **Fontes e metodologia** | Como o autor constrói o argumento, que fontes usa |
| **Argumento central** | Qual é a tese e como ela se desenvolve |
| **Conceitos-chave** | Que noções estruturam a análise e como o autor as usa |
| **Contexto e recorte** | Período, região, dimensão temática privilegiada |
| **Diálogo com a disciplina** | Como o texto se articula com a aula e o módulo |

Nem todas as dimensões precisam estar presentes em toda lista. Adaptar às
especificidades do texto e ao que é mais relevante para o debate em sala.

---

## Diretrizes gerais

- Questões abertas e discursivas — nunca de múltipla escolha ou verdadeiro/falso
- Cada questão deve exigir síntese ou paráfrase — evitar as que se respondem
  com um trecho copiado ou com "sim/não"
- Linguagem acessível ao nível de graduação em História
- A última questão pode ser mais aberta, articulando o texto com o tema da aula
  — verificar sempre em `ementa/ementa.md` antes de formulá-la
- Não inserir gabarito ou respostas esperadas no documento entregue ao estudante

---

## Procedimento de elaboração

1. Ler o texto disponível no contexto
2. Identificar a aula e o módulo correspondentes em `ementa/ementa.md`
3. Redigir entre 5 e 8 questões, cobrindo as dimensões relevantes para o texto
4. Revisar: cada questão deve ser respondível **apenas com o texto fornecido**
5. Revisar: nenhuma questão deve aceitar "sim/não" como resposta suficiente

---

## Formato de entrega

**Arquivo:** salvar em `bibliografia/apoio/` com nomenclatura:
`autor_ano_questoes-apoio.md` ou `autor_ano_questoes-PAGINAS.md`

**YAML frontmatter:**

```yaml
---
title: "Questões de apoio à leitura: Autor (ano)"
author: "Eric Brasil"
date: today
date-format: full
lang: pt-BR
---
```

**Corpo do documento:**

```markdown
**Autor, "Título abreviado", ano, pp. XX–XX**
Aula N | Tema da aula

---

1. Questão em parágrafo corrido.

2. Questão em parágrafo corrido.
```

Regras de formatação:
- Questões numeradas com `1.` simples — sem `**N.**`, sem blocos, sem seções temáticas
- Cada questão em parágrafo único, sem sub-itens
- Após gerar o `.md`, o docente renderiza para PDF; commitar ambos os arquivos

**Incluir na ementa** uma seção `**Material de apoio**` logo após as leituras
obrigatórias da aula correspondente:

```markdown
**Material de apoio**

* [Questões de apoio à leitura — Autor (ano)](../bibliografia/apoio/arquivo.pdf): roteiro com N perguntas sobre [...], para orientar a leitura e o debate em sala.
```
