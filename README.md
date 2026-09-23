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

### Fontes e fluxo editorial

Cada aula pode conter três arquivos relacionados:

```text
slides/aula-N/conteudo.md  # fonte editorial durante a revisão
slides/aula-N/index.qmd   # estrutura Quarto; sincronizada após aprovação
slides/aula-N/index.html  # apresentação standalone responsiva
slides/aula-N/assets/     # mídias locais específicas da aula
```

Enquanto a revisão estiver aberta, as alterações de conteúdo devem ser feitas em `conteudo.md`. O `index.qmd` legado permanece preservado até a aprovação docente; depois, o conteúdo aprovado é sincronizado para o `.qmd` e para o HTML final.

A apresentação responsiva não é gerada pelo Quarto: é uma **transposição editorial assistida**, não uma conversão automática genérica. O fluxo é:

1. Ler o material legado integralmente, preservando textos, datas, links, citações, bibliografia e sequência.
2. Registrar a versão editorial em `conteudo.md`, incluindo o recorte e o ponto de corte quando a aula vier de um deck anterior.
3. Converter as unidades aprovadas em seções semânticas no HTML (`<section class="slide">`).
4. Adaptar apenas a composição: hierarquia tipográfica, distribuição em colunas, janelas de imagens, legendas, navegação e comportamento móvel.
5. Copiar as mídias necessárias para `assets/`; sempre que possível, substituir GIFs pesados por MP4 local com `autoplay`, `muted`, `loop` e `playsinline`.
6. Comparar o conteúdo do HTML com `conteudo.md` e com o material legado, registrando qualquer fusão, divisão ou reorganização solicitada pelo docente.
7. Testar a apresentação em desktop e celular antes de publicar.

Exemplo atual:

- fonte editorial: `slides/aula-6/conteudo.md`;
- material legado preservado: `slides/aula-7/index.qmd`;
- apresentação standalone: `slides/aula-6/index.html`;
- 21 slides HTML, com encerramento sobre o tema da Aula 7.

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
- manter `conteudo.md`, `index.qmd` e `index.html` sincronizados somente após a aprovação da revisão;

---

## Licença

Distribuído sob licença [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).  
© [Eric Brasil, 2026](https://ericbrasil.com.br)

![](imgs/banner_logos_hist.png)
