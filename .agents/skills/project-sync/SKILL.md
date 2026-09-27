# Skill: Project Sync (Atualização de Projeto)

## Objetivo
Permitir que o usuário, a qualquer momento e por comando explícito, peça para o
agente analisar o estado atual de um projeto (código + conversa) e atualizar o
arquivo de memória correspondente em `vault/projetos/`. Não depende do fluxo de
abertura/encerramento de sessão da skill `daily-context`.

## Mecânicas Principais

### 1. Gatilho explícito, nunca automático
Esta skill só ativa quando o usuário pedir claramente, com frases como:
"atualiza o projeto", "analisa e atualiza", "atualiza a memória disso",
"salva o que fizemos aqui". Nunca roda por conta própria, por horário, ou
"aproveitando" outro comando.

### 2. Identificação do projeto em foco
Antes de escrever qualquer coisa, identifique qual projeto está em pauta:
- Pela pasta/arquivo que está aberto ou sendo discutido na conversa atual;
- Se houver ambiguidade (ex: mais de um projeto mencionado na sessão),
  pergunte qual antes de atualizar.

Se ainda não existir `vault/projetos/<nome-do-projeto>.md` para esse projeto,
crie um novo seguindo a mesma estrutura usada nos demais (não é preciso pedir
permissão para criar o arquivo, mas informe que ele foi criado).

### 3. Análise do estado real
Não confie apenas no que foi dito na conversa — quando possível, verifique o
código e/ou dados reais (arquivos do projeto, banco de dados, testes) antes de
decidir o que é "concluído" e o que é "pendente", da mesma forma que foi feito
ao investigar o sistema bibliotecário: ler o código de fato, não assumir pelo
que o usuário lembra.

### 4. Atualização incremental, não substituição total
Ao atualizar `vault/projetos/<nome>.md`:
- Preserve o que já estava correto em "Concluído" — apenas adicione o que
  mudou, não reescreva do zero;
- Mova para "Concluído" o que foi resolvido desde a última atualização;
- Atualize "Pendente" e "Dificuldade atual" com o que ficou em aberto;
- Atualize "Próximo passo" com base no que faz mais sentido atacar a seguir.

### 5. Transparência obrigatória
Depois de escrever, informe ao usuário exatamente o que mudou no arquivo antes
de seguir em frente — nunca atualizar em silêncio (regra global do
`GEMINI.md`).

## Regras de Ativação
- Só ativa mediante comando explícito do usuário — nunca em segundo plano,
  por gatilho de tempo, ou como efeito colateral de outro pedido.
- Não substitui a `daily-context`: aquela cuida do briefing de "bom
  dia"/"boa noite"; esta cuida do estado de um projeto específico, chamável a
  qualquer momento, independente da hora do dia.