# História da América: Colonização e Resistência – CCLHM0076

Repositório da disciplina **História da América: Colonização e Resistência**, ministrada pelo Prof. Eric Brasil no curso de Licenciatura em História do Instituto de Humanidades e Letras da UNILAB.

| Docente     | Período | CH  | Horário        | Sala | Contato                         |
|:-----------:|:-------:|:---:|:--------------:|:----:|:-------------------------------:|
| Eric Brasil | 2026.2  | 60h | Quintas, 8h30  | A definir | profericbrasil@unilab.edu.br    |

---

## Página online da disciplina

[História da América: Colonização e Resistência](https://ericbrasil.com.br/cclhm0076)

---

Versão atual, semestre 2026.2, no branch `2026_2`.

---

## Slides HTML responsivos

A partir de 2026.2, as apresentações podem utilizar um HTML responsivo próprio, projetado para ocupar toda a tela e funcionar tanto em computadores quanto em celulares.

### Fonte canônica

O arquivo Markdown/Quarto de cada aula permanece como referência principal do conteúdo:

```text
slides/aula-N/index.qmd   # fonte canônica: textos, ordem, citações e links
slides/aula-N/index.html  # apresentação responsiva publicada
slides/aula-N/assets/     # mídias locais específicas da aula
```

O HTML não substitui o `.qmd` como documento de autoria. Toda alteração de conteúdo deve ser feita primeiro no `.qmd` e depois transposta para o HTML.

### Como o HTML é gerado

A geração é uma **transposição editorial assistida**, não uma conversão automática genérica do Quarto. O fluxo é:

1. Ler integralmente `index.qmd`, incluindo o YAML, os separadores de slides e os blocos de conteúdo.
2. Usar cada slide do `.qmd` como unidade de referência, preservando textos, datas, links, citações, bibliografia e sequência.
3. Converter essas unidades em seções semânticas no HTML (`<section class="slide">`), aplicando o sistema visual responsivo da disciplina.
4. Adaptar apenas a composição: hierarquia tipográfica, distribuição em colunas, janelas de imagens, legendas, navegação e comportamento móvel.
5. Copiar as mídias necessárias para `assets/`; sempre que possível, substituir GIFs pesados por MP4 local com `autoplay`, `muted`, `loop` e `playsinline`.
6. Comparar o conteúdo do HTML com o `.qmd` e registrar explicitamente qualquer fusão, divisão ou reorganização solicitada pelo docente.
7. Testar a apresentação em desktop e celular antes de publicar.

A Aula 1 é o primeiro exemplo desse formato:

- fonte: `slides/aula-1/index.qmd`;
- apresentação publicada: `slides/aula-1/index.html`;
- 35 slides HTML, incluindo um encerramento com o tema da aula seguinte.

### Atenção ao Quarto

Não execute diretamente:

```bash
quarto render slides/aula-1/index.qmd
```

Esse comando gera um novo RevealJS e **sobrescreve** o `index.html` responsivo. O `.qmd` deve ser mantido como fonte de conteúdo, enquanto a atualização do HTML segue o fluxo editorial descrito acima.

### Requisitos de verificação

Antes de commitar uma apresentação:

- conferir que o HTML cobre todo o conteúdo do `.qmd`;
- testar navegação por teclado, botões, hash e gesto de swipe;
- testar, no mínimo, em 1440×900 e 390×844;
- confirmar ausência de overflow horizontal e erros de console;
- verificar carregamento de logos, imagens, vídeos e QR code;
- manter o `.qmd` no commit sempre que houver alteração de conteúdo.

---

## Licença

Distribuído sob licença [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).  
© [Eric Brasil, 2026](https://ericbrasil.com.br)

![](imgs/banner_logos_hist.png)
