# Biblioteca Digital

Sistema simples de gerenciamento de livros, desenvolvido em Python com
CustomTkinter.

## 1. Sobre o projeto

O projeto **Biblioteca Digital** tem como objetivo facilitar a
organização de livros e o controle de um acervo. A aplicação possui uma
interface gráfica para cadastrar, pesquisar e visualizar livros.

**Matéria:** Programação e Empreendedorismo\
**Linguagem:** Python\
**Biblioteca gráfica:** CustomTkinter

## 2. Escopo

### Objetivo

Criar uma ferramenta simples e prática para ajudar bibliotecas a
organizar seus livros e controlar os empréstimos.

### Público-alvo

-   Bibliotecas escolares;
-   Estudantes;
-   Funcionários responsáveis pelo acervo.

### Funcionalidades previstas

-   Cadastro de livros com título, autor e categoria;
-   Consulta dos livros cadastrados;
-   Pesquisa de livros pelo título;
-   Identificação de livros disponíveis ou emprestados;
-   Registro de empréstimos e devoluções (etapas futuras de
    desenvolvimento).

## 3. Fluxograma

``` mermaid
flowchart TD
    A([Iniciar sistema]) --> B[Exibir menu principal]
    B --> C{Escolher opção}
    C -->|Cadastrar| D[Informar dados do livro]
    D --> E[Salvar livro]
    E --> B
    C -->|Consultar| F[Mostrar livros cadastrados]
    F --> B
    C -->|Pesquisar| G[Digitar nome do livro]
    G --> H{Livro encontrado?}
    H -->|Sim| I[Exibir informações]
    H -->|Não| J[Exibir mensagem não encontrado]
    I --> B
    J --> B
    C -->|Empréstimo| K[Registrar empréstimo]
    K --> B
    C -->|Devolução| L[Registrar devolução]
    L --> B
    C -->|Sair| M([Encerrar sistema])
```

## 4. Prototipagem

A interface foi planejada com CustomTkinter, utilizando uma tela
principal com:

-   Título da aplicação;
-   Campos para título, autor e categoria;
-   Área para exibir os livros cadastrados;
-   Botões para cadastrar, pesquisar e listar os livros.

### Exemplo de visualização

``` text
+-----------------------------------------------+
|               BIBLIOTECA DIGITAL              |
|                                               |
|              [Título do livro]                |
|              [Nome do autor]                  |
|              [Categoria]                      |
|                                               |
|              [Cadastrar Livro]                |
|              [Pesquisar Livro]                |
|              [Mostrar Todos]                  |
|                                               |
|              LIVROS CADASTRADOS               |
|  Dom Casmurro - Machado de Assis - Disponível |
+-----------------------------------------------+
```

## 5. Tecnologias utilizadas

-   **Python 3** --- linguagem de programação;
-   **CustomTkinter** --- criação da interface gráfica;
-   **Tkinter** --- caixas de mensagens.

## 6. Como executar

1.  Instale o Python 3.

2.  Abra o terminal na pasta do projeto.

3.  Instale a dependência:

    ``` bash
    pip install -r requirements.txt
    ```

4.  Execute o programa:

    ``` bash
    python app.py
    ```

## 7. Código-fonte

O código principal está no arquivo [`app.py`](app.py).

## 8. Limitações e próximas melhorias

Esta é uma versão inicial de protótipo. Os livros ficam armazenados
apenas na memória enquanto o programa está aberto. Ao fechar a
aplicação, os dados cadastrados são perdidos.

Possíveis melhorias para versões futuras:

-   Salvar os livros em um banco de dados;
-   Implementar o registro de empréstimos;
-   Implementar o registro de devoluções;
-   Impedir empréstimos de livros que já estejam emprestados;
-   Adicionar edição e exclusão de livros.

## 9. Conclusão

O projeto Biblioteca Digital propõe uma solução simples para apoiar a
organização de bibliotecas escolares. Com Python e CustomTkinter, o
protótipo permite cadastrar, pesquisar e consultar livros por meio de
uma interface gráfica. O desenvolvimento também oferece uma oportunidade
de aplicar conceitos de programação, lógica e organização de sistemas.
