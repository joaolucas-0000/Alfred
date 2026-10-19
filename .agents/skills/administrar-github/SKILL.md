---
name: administrar-github
description: Consulta e prepara operações controladas em repositórios GitHub por meio do MCP existente.
---

# Administrar GitHub

## Objetivo

Consultar e preparar operações de repositório usando exclusivamente o MCP do GitHub já configurado.

## Quando usar

Use para consultar repositórios, branches, commits, issues ou pull requests; analisar alterações; preparar commits; criar branch quando autorizada; ou acompanhar CI quando disponível.

## Quando não usar

Não use para configurar integrações, manipular credenciais, alterar configurações críticas, fazer merge automático, sobrescrever histórico ou excluir repositórios.

## Entradas esperadas

Repositório e objetivo da consulta ou operação; branch e escopo das mudanças para escrita; aprovação explícita quando houver efeito externo.

## Ferramentas permitidas

Somente ferramentas do MCP do GitHub já disponível e ferramentas locais de leitura de diff/status. Não configure servidores, não solicite credenciais e não presuma recursos que a ferramenta não exponha.

## Procedimento

1. Identifique o repositório, branch e objetivo; em caso de ambiguidade, não faça escrita.
2. Para consultas solicitadas, leia os dados disponíveis e cite identificadores ou URLs retornados pelo MCP.
3. Para alterações, analise primeiro o estado e o diff local e prepare um resumo do impacto.
4. Apresente o resumo e obtenha aprovação explícita para cada escrita externa: criar issue, branch remota, commit, push ou pull request.
5. Evite a branch principal e respeite proteções; use branch específica quando autorizada.
6. Antes de commit autorizado, verifique diff e status e use mensagem descritiva.
7. Execute apenas a operação aprovada por meio do MCP. Nunca faça force push, merge automático, exclusão de repositório ou alterações críticas.
8. Acompanhe CI se a ferramenta fornecer essa capacidade e informe somente o estado retornado.

## Aprovações necessárias

Leituras não exigem aprovação adicional além do pedido do usuário. Toda escrita no GitHub exige aprovação explícita prévia para aquela operação. Nunca altere secrets, tokens, webhooks, equipes, colaboradores ou configurações críticas.

## Validação do resultado

Valide a resposta do MCP e, quando possível, releia o recurso ou estado resultante. Informe URL ou identificador retornado. Não afirme conclusão com base apenas na intenção de executar.

## Tratamento de erros

Em falha ou resposta ambígua, preserve o estado, verifique se houve efeito antes de qualquer nova tentativa e relate a resposta observada. Não repita escrita incerta.

## Formato de saída

Informe repositório e branch, resumo da consulta ou mudança, aprovação recebida, validação, identificador/URL quando retornado e pendências.

## Exemplos de uso

- Consultar commits recentes de uma branch solicitada.
- Analisar um diff e preparar uma proposta de commit, sem enviá-la antes da aprovação.