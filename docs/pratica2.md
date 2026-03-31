# Prática 2 — Respostas

## 1. Qual a vantagem de gerar dados fake em vez de usar dados reais neste laboratório?

Permite testar e validar pipelines sem expor dados sensíveis ou depender de dados reais, garantindo privacidade e flexibilidade.

## 2. Qual é o papel do Workflow no Temporal?

Orquestrar a sequência de atividades, controlando o fluxo, dependências e tratamento de falhas do pipeline.

## 3. Qual a diferença entre Workflow e Activity?

Workflow define o fluxo e lógica de orquestração; Activity executa tarefas específicas (ex: gerar CSV, carregar no banco).

## 4. O que muda quando o destino sai de um banco local e passa para o Atlas?

A persistência passa a ser em nuvem, exigindo conexão segura, configuração de acesso e maior atenção à latência e segurança.

## 5. Esse pipeline já pode ser considerado pronto para produção? O que ainda falta?

Não. Faltam validações robustas, logging estruturado, tratamento de erros, testes automatizados, monitoramento, autenticação segura e deploy automatizado.
