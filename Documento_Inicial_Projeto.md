# Documento Inicial do Projeto — Sistema de Gestão de Estoque

## Equipe

| Integrante | Função |
|---|---|
| Waldison | Integrante da equipe |
| Joabe | Integrante da equipe |

## 1. Entendimento do problema

Uma pequena empresa comercializa produtos de diferentes categorias e atualmente controla o estoque de forma manual. Com o crescimento da empresa, esse controle ficou mais difícil.

Os principais problemas são o cadastro de produtos, consulta e localização de produtos, controle das quantidades, identificação de estoque baixo, alteração de informações e cálculo do valor total do estoque.

O sistema terá como objetivo organizar essas informações e facilitar o controle básico do estoque.

A primeira versão poderá funcionar localmente e poderá utilizar uma interface de linha de comando.

## 2. Objetivo do sistema

Desenvolver uma primeira versão de um Sistema de Gestão de Estoque utilizando Java, permitindo controlar produtos e suas quantidades em estoque.

A solução também deverá ser organizada de forma que possa receber novas funcionalidades futuramente.

## 3. Requisitos Funcionais

### RF01 — Cadastro de produto

O sistema deverá permitir cadastrar um produto com:

- código;
- descrição;
- preço;
- quantidade em estoque.

O código deverá ser único para cada produto.

### RF02 — Consulta de produto

O usuário deverá conseguir consultar um produto informando seu código.

Caso o produto não exista, o sistema deverá informar essa situação.

### RF03 — Listagem de produtos

O sistema deverá apresentar os produtos cadastrados, mostrando pelo menos:

- código;
- descrição;
- preço;
- quantidade disponível.

### RF04 — Alteração de produto

O usuário deverá conseguir alterar as informações de um produto cadastrado.

### RF05 — Exclusão de produto

O sistema deverá permitir remover um produto quando necessário.

### RF06 — Entrada de estoque

O sistema deverá permitir registrar a entrada de produtos no estoque.

### RF07 — Saída de estoque

O sistema deverá permitir registrar a saída de produtos.

A quantidade retirada não poderá ser maior que a quantidade disponível.

### RF08 — Estoque mínimo

O sistema deverá permitir identificar produtos que estejam abaixo de uma quantidade mínima definida para o projeto.

### RF09 — Valor do estoque

O sistema deverá calcular o valor total dos produtos armazenados utilizando:

**Valor do estoque = preço × quantidade**

## 4. Requisitos Não Funcionais

### RNF01 — Linguagem

A aplicação deverá ser desenvolvida em Java.

### RNF02 — Organização

O código deverá possuir uma organização adequada e responsabilidades separadas de forma coerente.

### RNF03 — Legibilidade

O código deverá utilizar nomes claros, organização lógica, indentação adequada e evitar repetição desnecessária.

### RNF04 — Tratamento de situações inválidas

O sistema deverá tratar situações como:

- produto inexistente;
- código duplicado;
- quantidade inválida;
- preço inválido;
- saída maior que o estoque;
- entrada de dados inválida.

### RNF05 — Versionamento

O projeto deverá utilizar Git e GitHub para registrar a evolução do desenvolvimento e a participação dos integrantes.

### RNF06 — Documentação

O projeto deverá possuir documentação sobre o objetivo, funcionalidades, execução, decisões importantes e estrutura da aplicação.

## 5. Atores

### Usuário

Pessoa que utilizará o sistema para cadastrar, consultar, alterar, excluir e controlar os produtos e o estoque.

## 6. Casos de uso iniciais

O usuário poderá:

1. Cadastrar produto;
2. Consultar produto;
3. Listar produtos;
4. Alterar produto;
5. Excluir produto;
6. Registrar entrada de estoque;
7. Registrar saída de estoque;
8. Verificar estoque mínimo;
9. Calcular valor total do estoque.

## 7. Modelo inicial da solução

A primeira ideia do grupo é trabalhar com uma estrutura simples, começando pelo produto e pelo controle do estoque.

```text
Usuário
   |
   +-- Cadastrar produto
   +-- Consultar produto
   +-- Listar produtos
   +-- Alterar produto
   +-- Excluir produto
   +-- Entrada de estoque
   +-- Saída de estoque
   +-- Verificar estoque mínimo
   +-- Calcular valor do estoque
```

Esse modelo poderá ser melhorado conforme o projeto evoluir e os primeiros diagramas UML forem desenvolvidos.

## 8. Decisões iniciais

### DEC01 — Código único do produto

O produto será identificado por um código único para facilitar a consulta e evitar produtos diferentes com o mesmo código.

### DEC02 — Primeira versão local

A primeira versão poderá funcionar localmente, conforme permitido pela RFP. Não será necessário criar inicialmente um sistema web ou uma interface gráfica.

### DEC03 — Java

O projeto será desenvolvido em Java, pois essa é uma exigência da RFP.

### DEC04 — Evolução futura

A estrutura inicial deverá permitir que novas partes sejam adicionadas futuramente, como clientes, fornecedores, pedidos, usuários, funcionários, relatórios, vendas e compras.

## 9. Como os dados serão tratados inicialmente

Nesta primeira etapa, o grupo pretende manter a solução simples para entender primeiro o problema e os requisitos. A forma definitiva de armazenamento será definida conforme o projeto evoluir.

## 10. Possíveis evoluções

No futuro, o sistema poderá receber módulos para:

- clientes;
- fornecedores;
- pedidos;
- usuários;
- funcionários;
- movimentações de estoque;
- relatórios;
- vendas;
- compras.

## 11. Primeiras Issues sugeridas

- `[REQ] Levantar requisitos funcionais`
- `[REQ] Levantar requisitos não funcionais`
- `[UML] Identificar ator e casos de uso`
- `[UML] Criar primeiro modelo de casos de uso`
- `[DOC] Documentar entendimento do problema`
- `[DOC] Registrar decisões iniciais`

## 12. Respostas ao desafio inicial

### 1. Quais são as principais entidades identificadas?

A principal entidade identificada inicialmente é **Produto**. O **Estoque** também representa uma parte importante do problema, pois controla as quantidades e movimentações dos produtos.

### 2. Quais informações devem ser armazenadas?

Para cada produto, inicialmente serão armazenados código, descrição, preço e quantidade em estoque.

### 3. Quais operações o sistema precisa realizar?

Cadastro, consulta, listagem, alteração, exclusão, entrada de estoque, saída de estoque, verificação de estoque mínimo e cálculo do valor total do estoque.

### 4. Como os dados serão armazenados?

A forma de armazenamento será definida durante a evolução do projeto. Nesta primeira etapa, o grupo irá priorizar o entendimento dos requisitos e uma solução simples.

### 5. Como o sistema poderá crescer?

A solução deverá ser organizada de maneira que novos módulos possam ser adicionados sem precisar refazer todo o sistema. Entre as futuras possibilidades estão clientes, fornecedores e pedidos.

### 6. Quais partes provavelmente precisarão ser alteradas no futuro?

A parte responsável pelo armazenamento e as regras relacionadas às novas entidades poderão precisar de alterações. Por isso, o grupo pretende separar as responsabilidades conforme o projeto evoluir.

## 13. Próximos passos

1. Criar e revisar as Issues iniciais.
2. Revisar os requisitos com todos os integrantes.
3. Criar o primeiro diagrama de casos de uso.
4. Registrar as decisões do grupo.
5. Fazer o primeiro commit da documentação.
6. Depois iniciar a implementação da primeira versão.

## 14. Referências utilizadas

- RFP — Desenvolvimento de Sistema de Gestão de Estoque.
- Manual de Início do Projeto — Engenharia de Software + Programação Avançada.
- Manual de Trabalho com GitHub — FATEC Tatuí / Itu / Indaiatuba.
