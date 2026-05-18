# Sistema Escolar - Validação em JavaScript

Este repositório contém a conversão de um sistema de cadastro de alunos, originalmente desenvolvido em PHP, para uma aplicação front-end utilizando HTML e JavaScript (manipulando o `localStorage`).

## Localização da Validação de Matrícula

A lógica principal tá dentro da tag `<script>`, mais especificamente na função chamada `validarMatricula`.

A função recebe como parâmetros o valor digitado no campo de matrícula e o vetor de alunos já cadastrados no sistema. Ela realiza três verificações --> 

1. **Preenchimento obrigatório:** Verifica se o campo está vazio.
2. **Apenas números:** Utiliza uma Expressão Regular (`/^\d+$/`) para garantir que o usuário digitou apenas caracteres numéricos.
3. **Prevenção de duplicidade:** Percorre a lista de alunos salvos no `localStorage` e verifica se a matrícula informada já existe no banco de dados local.

Se qualquer uma dessas regras for violada, a função retorna uma mensagem de erro em formato de texto, que é exibida imediatamente na interface do usuário. Caso a matrícula atenda a todos os critérios, a função retorna `null`, liberando o fluxo para a conclusão do cadastro.
Esse exercício foi passado em aula pelo professor André Neves - FAETERJ.
