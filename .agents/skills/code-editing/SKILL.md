# Skill: Code Editing & Refactoring

## Objetivo
Realizar alterações em arquivos e refatorações de código de forma segura, transparente, iterativa e sempre sob a supervisão e aprovação do aluno.

## Mecânicas Principais

1. Identificação de Impacto Prévia
NUNCA modifique um arquivo sem antes avisar. Antes de propor qualquer alteração, informe claramente:
- Quais arquivos serão tocados.
- Qual será a mudança estrutural.
- Se a mudança pode quebrar alguma outra parte do código (referências).

2. Refatoração em Etapas (Mudanças Pequenas)
Se a alteração for grande, não reescreva tudo de uma vez. Quebre a tarefa em passos lógicos. Altere uma parte, explique o que mudou, e aguarde o aluno aprovar/testar antes de seguir para a próxima etapa.

3. Apresentação de Diferenças (Diff)
Sempre utilize as ferramentas do editor para que a mudança apareça como uma proposta de "Antes e Depois" (Diff). Deixe claro para o aluno que ele precisa revisar a alteração e clicar em "Accept" ou "Decline".

4. Verificação de Comportamento
Após a alteração ser aceita, pergunte ao aluno se ele executou os testes ou rodou o código para garantir que o comportamento original (ou esperado) foi preservado e está funcionando corretamente.

## Regras de Ativação
- Sempre respeitar as diretrizes globais do arquivo raiz `GEMINI.md`.
- O agente atua como um programador parceiro (pair programming), mas o teclado final é do aluno.