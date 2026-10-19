---
name: executar-tarefa
description: Executa tarefas locais simples e coordena capacidades do Alfred sem substituir procedimentos especializados.
---

# Executar tarefa

## Objetivo

Executar tarefas locais simples relacionadas às capacidades do Alfred e coordenar etapas sem duplicar procedimentos de outras skills.

## Quando usar

Use para solicitações locais simples, verificações e coordenação de uma tarefa que não seja principalmente pesquisa, notícias, organização de arquivos ou GitHub.

## Quando não usar

Não use como substituta de `pesquisar-internet`, `ler-noticias`, `organizar-arquivos` ou `administrar-github`. Não use esta skill para contornar permissões ou aprovações especializadas.

## Entradas esperadas

Objetivo esperado, escopo autorizado, arquivos ou recursos envolvidos e restrições fornecidas pelo usuário.

## Ferramentas permitidas

Ferramentas locais disponibilizadas pelo ambiente para inspecionar, editar e verificar arquivos. Use ferramentas externas somente através da skill especializada e da integração já disponível.

## Procedimento

1. Defina o resultado esperado e confirme o escopo.
2. Leia os arquivos e instruções relevantes antes de editar.
3. Elabore um plano proporcional; não apresente um plano formal para tarefa trivial.
4. Selecione outra skill apenas quando uma etapa especializada for necessária.
5. Execute somente as ações necessárias, preservando conteúdo não relacionado.
6. Verifique o resultado e registre os artefatos criados ou modificados.

## Aprovações necessárias

Obtenha aprovação explícita para exclusões, substituições, movimentações em massa, acesso fora do escopo ou qualquer operação externa de escrita. Aplicam-se também as regras da skill especializada.

## Validação do resultado

Confirme o estado final com uma leitura, teste ou inspeção adequada ao pedido. Não declare sucesso sem evidência; relate falhas e resultados parciais.

## Tratamento de erros

Interrompa a etapa afetada, preserve os dados, descreva o erro observado e informe as ações que ficaram pendentes. Não invente uma saída substituta.

## Formato de saída

Resumo do resultado, verificação, arquivos criados ou modificados e limitações. Salve um artefato em `workspace/saida` quando solicitado ou necessário, não automaticamente.

## Exemplos de uso

- Conferir se um arquivo de saída foi criado após uma tarefa autorizada.
- Preparar um relatório local curto usando resultados já verificados.
- Coordenar uma solicitação simples que não demande procedimento especializado.
