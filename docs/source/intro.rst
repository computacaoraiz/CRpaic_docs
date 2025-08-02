**********
Introdução
**********

.. note::

   This project is under active development. The docs are not finished yet.
   Please, be patient.

.. highlight:: c

.. hint::
   
   * Para **estudantes**: se você é um estudante ou é um programador que
     pretende apenas *usar* a CRpaic, você pode ignorar este capítulo com
     segurança, pois as informações aqui são mais úteis para professores.
   * Para **professores**: se você é um professor, este capítulo contém
     informações importantes sobre a biblioteca e deve ser lido, pois discute o
     que é a biblioteca, a motivação para sua criação, questões de instalação e
     desinstalação, compilação, plataformas e outras informações técnicas
     importantes.

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
:code:`crpaic_get_string`. Isso permite que alunos absolutamente iniciantes
consigam criar programas como o :file:`ola.c`, abaixo::

    #include <CRpaic.h>
    #include <stdio.h>

    int main (void)
    {
        string nome = crpaic_get_string("Informe seu nome: ");
        printf("Olá, %s!\n", nome);
    }

A compilação é feita com GCC ou Clang, fazendo a vinculação com a CRpaic:

.. code-block:: bash

   $ gcc -std=c17 -Wall -Wpedantic -Werror -o ola ola.c -lCRpaic
  
Ao ser executado na linha de comando, o programa resulta em:

.. code-block:: bash

   $ ./ola
   Informe seu nome: Abrantes
   Olá, Abrantes!

A variável :code:`nome` no código acima é do tipo :code:`string`, mas esse tipo
é, na verdade, um alias para um ponteiro para um caractere. A função
:code:`crpaic_get_string` exibe um prompt para o usuário, obtém a string
informada na linha de comando, aloca memória na *heap*, coloca a string nessa
área de memória e retorna o ponteiro de acesso à string. Ao final do programa
essa área de memória é liberada e desalocada automaticamente pela biblioteca,
evitando-se assim vazamento de memória e ponteiros pendurados. E tudo isso é
feito de modo automático para o estudante iniciante, que trata a variável
:code:`nome` como se fosse um tipo primitivo qualquer da linguagem C. Quando
esse estudante alcançar maior maturidade na linguagem o professor pode revelar o
tipo de dado subjacente (:code:`char *`), as funções de I/O (:code:`fgetc`,
:code:`scanf`, :code:`getc`, etc.), as funções de gerenciamento de memória
(:code:`malloc`, :code:`free`, etc.) e funcionalidades mais avançadas da
linguagem, se necessário.

Com a CRpaic é possível ensinar conceitos de computação e programação usando a
linguagem C para estudantes realmente iniciantes (estudantes no 1º período da
graduação, por exemplo), já que a biblioteca esconde muito da complexidade de C
até que os estudantes estejam melhor equipados para compreender como tudo
funciona realmente.

==========
Por que C?
==========

Com tantas linguagens mais modernas e amigáveis para os estudantes, como Python,
Java e outras, por que utilizar C para estudantes iniciantes?

Essas é uma discussão que já foi travada incontáveis vezes por todos os
professores de computação e/ou programação, com argumentos favoráveis e
desfavoráveis de todos os tipos. Minha experiência como professor de diversas
disciplinas de computação (introdução à ciência da computação, linguagens de
programação, sistemas operacionais, arquitetura de computadores) me fez optar
por C pelas seguintes razões:

* É uma linguagem pequena e simples de aprender: como C tem poucas *keywords* e
  poucos operadores, em pouco tempo o estudante iniciante consegue utilizar a
  maioria dos construtos da linguagem.
* É uma linguagem compilada, o que força os estudantes a enxergar claramente a
  diferença entre o código fonte e o código executável. O entendimento do
  processo de compilação é, por si só, um benefício considerável.
* É uma linguagem de alto nível que não esconde detalhes voltados ao hardware,
  como ponteiros e alocação de memória. Estudantes que conhecem esses detalhes
  estão mais preparados para disciplinas como arquitetura de computadores ou
  sistemas operacionais. Esse fato é corroborado por minha própria experiência
  pessoal: com muita freqüência recebo alunos com background em C ou com
  background em Python na disciplina de Arquitetura de Computadores e,
  invariavelmente, os alunos com background em C entendem e se saem melhor do
  que os alunos com background em Python.
* A necessidade de preparar os estudantes para disciplinas mais práticas nas
  quais os mesmos constroem dispositivos com microcontroladores stand-alone ou
  usando placas como o Arduino ou ESP32. A programação de microcontroladores é
  feita, em geral, com C ou C++ e, portanto, alunos que aprendem desde cedo a
  programar em C têm um forte background para essas disciplinas.
* Eu gosto.


============
Installation
============

xxx

==================
Development status
==================

xxx
