************
Introduction
************

.. note::

   This project is under active development. The docs are not finished yet.
   Please, be patient.

.. highlight:: c

A biblioteca **CRpaic** é uma biblioteca C voltada para estudantes de computação
e programadores iniciantes que queiram utilizar a linguagem C como meio de
aprendizagem de conceitos fundamentais da ciência da computação e da
programação.

A grosso modo a CRpaic objetiva "adocicar" um pouco a linguagem C fornecendo
abstrações e funções que facilitam o aprendizado e o uso dessa linguagem por
estudantes iniciantes, libertando-os dos detalhes mais internos e obscuros da
sintaxe e semântica de C, para permitir que o foco do aprendizado sejam os
conceitos importantes da computação e programação.

Considere um exemplo: alunos iniciantes têm muita dificuldade de entender o
conceito de "string" como um array de caracteres em C e, mais ainda, a diferença
entre usar arrays de caracteres diretamente (:code:`char nome[20];`) ou usar um
ponteiro para um caractere (:code:`char *nome;`). CRpaic resolve isso fornecendo
uma abstração para strings, o tipo de dado :code:`string`, e uma função para
solicitar uma string ao usuário após um prompt amigável, a função
:code:`crpaic_get_string()`. Isso permite que alunos absolutamente iniciantes
consigam criar programas como o seguinte::

    #include <CRpaic>
    #include <stdio.h>

    int main (void)
    {
        string nome = crpaic_get_string("Informe seu nome: ");
        printf("Olá, %s!\n", nome);
    }

A variável :code:`nome` no código acima é do tipo :code:`string`, mas esse tipo
é, na verdade, um alias para um ponteiro para um caractere. A função
:code:`crpaic_get_string()` exibe um prompt para o usuário, obtém a string
informada na linha de comando, aloca memória na *heap*, coloca a string nessa
área de memória e retorna o ponteiro de acesso à string. Ao final do programa
essa área de memória é liberada e desalocada automaticamente pela biblioteca,
evitando-se assim vazamento de memória e ponteiros pendurados. E tudo isso é
feito de modo automática para o estudante iniciante, que trata a variável
:code:`nome` como se fosse um tipo primitivo qualquer da linguagem C. Quando
esse estudante alcançar maior maturidade na linguagem o professor pode revelar o
tipo de dado subjacente (:code:`char *`), as funções de I/O (:code:`fgetc`,
:code:`scanf`, :code:`getc`, etc.), as funções de gerenciamento de memória
(:code:`malloc`, :code:`free`, etc.) e funcionalidades mais avançadas da
linguagem.

============
About CRpaic
============

xxx

============
Installation
============

xxx

==================
Development status
==================

xxx
