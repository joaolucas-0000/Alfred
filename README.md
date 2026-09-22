# Projeto Alfred

Bem-vindo ao projeto Alfred! O Alfred é um agente inteligente projetado para receber solicitações do usuário, entender objetivos, planejar a execução de tarefas, utilizar skills (habilidades) disponíveis e delegar atividades especializadas para subagentes quando necessário.

## Visão Geral

O foco principal do Alfred é automatizar e auxiliar na execução de tarefas locais, atuando de maneira segura e estruturada dentro do seu próprio ecossistema. Ele segue um fluxo rigoroso de planejamento, execução, delegação e verificação de resultados.

## Estrutura do Projeto

Abaixo estão os principais diretórios e arquivos que compõem o ambiente do projeto:

- **`.agents/rules/Alfred.md`**: Define o comportamento e limites permanentes. O sistema reconhece regras locais no diretório `.agents/rules/`.
- **`.agents/skills/`**: Contém as habilidades (skills) que o agente pode utilizar. Cada skill possui seu próprio diretório e um arquivo `SKILL.md`.
  - Exemplo: `.agents/skills/executar-tarefa/SKILL.md` (procedimento para executar e verificar tarefas).
  - Exemplo: `.agents/skills/pesquisar-internet/SKILL.md` (pesquisa de informações).
- **`agents/assistente.md`**: Rascunho do agente principal ou de subagentes em desenvolvimento.
- **`workspace/entrada/`**: Diretório destinado aos arquivos iniciais ou dados fornecidos pelo usuário para processamento.
- **`workspace/saida/`**: Diretório onde os resultados finais gerados pelo agente são salvos de forma segura.
- **`README.md`**: Este arquivo, com a descrição do projeto e sua estrutura.

## Como Funciona (Fluxo de Trabalho)

1. **Compreensão e Planejamento**: O Alfred recebe a solicitação e elabora um plano de ação estruturado.
2. **Execução e Delegação**: Utiliza as skills apropriadas para a tarefa ou delega atividades complexas (como pesquisas na internet) para agentes especializados (ex: Agente Pesquisador).
3. **Segurança e Limites**: Trabalha exclusivamente dentro da pasta do projeto, respeitando permissões, e sempre solicita autorização para ações destrutivas ou externas.
4. **Verificação**: Avalia os resultados produzidos antes de apresentá-los.
5. **Entrega**: Disponibiliza os artefatos finais em `workspace/saida` e detalha os arquivos modificados e as ações realizadas.

## Segurança e Limitações

- O agente opera apenas dentro do diretório deste projeto (`Alfred`).
- Não realiza instalação de programas, exclusão permanente de arquivos ou modificações no sistema operacional sem autorização explícita do usuário.
- Comandos destrutivos e acessos a credenciais ou tokens são estritamente proibidos e bloqueados pela política do projeto.