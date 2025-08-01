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
:code:`crpaic_get_string()`:

:code:`string nome = crpaic_get_string("Informe seu nome: ");`

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
