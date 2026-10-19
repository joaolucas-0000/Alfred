---
name: organizar-arquivos
description: Analisa e organiza arquivos locais com prévia, rastreabilidade e operações reversíveis.
---

# Organizar arquivos

## Objetivo

Analisar, classificar e organizar arquivos locais sem alterar conteúdo ou perder dados.

## Quando usar

Use para inspecionar, agrupar, mover ou renomear arquivos em diretórios autorizados pelo ambiente.

## Quando não usar

Não use para editar o conteúdo dos arquivos, acessar diretórios de sistema, seguir links para fora do escopo ou excluir duplicados. Alterações de conteúdo devem ser solicitadas separadamente.

## Entradas esperadas

Diretório autorizado, objetivo da organização, critérios de classificação e indicação de se o usuário quer apenas uma proposta ou execução.

## Ferramentas permitidas

Ferramentas locais de listagem, leitura de metadados e movimentação disponibilizadas pelo ambiente. Não use ferramentas externas para transferir arquivos.

## Procedimento

1. Inspecione apenas o escopo autorizado e classifique por tipo, finalidade, projeto ou data, conforme o objetivo.
2. Identifique possíveis duplicados sem excluí-los e preserve extensões.
3. Para mudanças amplas, apresente prévia com origem, destino, ação, motivo e conflitos; aguarde aprovação antes de executá-las.
4. Verifique conflitos de nomes e confirme que nenhum destino será sobrescrito.
5. Prefira movimentação reversível; registre origem, destino e motivo de cada operação.
6. Não altere o conteúdo dos arquivos.
7. Após a execução autorizada, valide a existência do destino e informe o status de cada item.

## Aprovações necessárias

Peça aprovação explícita antes de movimentações em massa, substituições ou exclusões. Exclusões permanentes não são permitidas. Siga também `.agents/rules/filesystem.md`.

## Validação do resultado

Confirme origem e destino, conflitos e existência dos arquivos após a operação. Relate itens não processados e preserve a lista de operações para permitir reversão.

## Tratamento de erros

Pare a operação afetada, não sobrescreva nem apague dados, registre o erro e informe quais itens foram ou não movidos. Se o estado for ambíguo, inspecione antes de repetir.

## Formato de saída

Relatório em tabela ou lista com origem, destino, ação, motivo e status; inclua conflitos, duplicados possíveis e validação.

## Exemplos de uso

- Propor uma organização por tipo para uma pasta autorizada antes de mover arquivos.
- Agrupar documentos por ano, preservando nomes, extensões e rastreabilidade.