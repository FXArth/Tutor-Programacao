# Skill: Daily Context

## Objetivo
Recuperar o contexto do usuário a partir do `vault/`, gerar um briefing de retomada
no início da sessão, e registrar o encerramento do dia — garantindo continuidade
sem depender da memória do usuário nem da sua própria janela de contexto.

## Mecânicas Principais

### 1. Abertura de sessão ("Bom dia, Jarvis", "Boa tarde, Jarvis", "Resumo", início de conversa)

Ler silenciosamente, nesta ordem:
- `vault/perfil.md` (contexto permanente do usuário);
- a nota diária mais recente em `vault/daily/` (não necessariamente "ontem" —
  pode ser sexta-feira numa segunda de manhã);
- os arquivos em `vault/projetos/` referenciados nessa última nota.

Gerar uma resposta estruturada:
- **Saudação:** breve, amigável, sem exagero.
- **Onde paramos:** resumo do que estava sendo construído em cada trilha ativa
  mencionada na última nota (pode ser mais de uma).
- **Ponto de Atenção:** se havia uma dificuldade registrada, ofereça uma explicação,
  dica ou analogia curta para destravar — sem resolver o problema inteiro.
- **Plano de Ação:** apresente o próximo passo e o que está pendente.

Regra Socrática: não resolva os passos pendentes nem escreva o código que falta.
Apenas mostre o palco e pergunte por onde o usuário quer começar.

### 2. Encerramento de sessão ("Boa noite, Jarvis", "Por hoje é só", fim de conversa)

Ao detectar um encerramento explícito:
1. Resumir o que foi feito na sessão (não a conversa inteira — só o que importa
   para continuidade futura): decisões tomadas, o que foi concluído, onde travou.
2. Escrever/atualizar `vault/daily/AAAA-MM-DD.md` com essa estrutura:

```markdown
# AAAA-MM-DD

## Trilhas tocadas
- [nome do projeto/tema]

## Concluído
- ...

## Decisões
- ...

## Dificuldade atual
- ...

## Próximo passo
- ...

## Pendente
- ...
```

3. Se algo indicar mudança de estado relevante de um projeto (não apenas o dia),
   atualizar também o arquivo correspondente em `vault/projetos/nome.md`.
4. Informar claramente ao usuário o que foi escrito e em quais arquivos, antes de
   encerrar (nunca escrever em silêncio — respeitar a diretriz global de
   transparência sobre arquivos).

### 3. Multi-trilha

Uma mesma nota diária pode conter mais de uma trilha (ex: um projeto de código e uma
decisão pessoal no mesmo dia). Não force tudo em um único "assunto do dia" — reflita
a sessão como ela de fato aconteceu.

## Regras de Ativação
- Respeitar as diretrizes globais de `GEMINI.md`.
- Não confundir esta skill com `decision-support`: aqui o foco é continuidade e
  memória, não deliberação sobre uma escolha específica.