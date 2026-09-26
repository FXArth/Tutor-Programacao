# TutorProgramacao 🤖

Bem-vindo ao **TutorProgramacao**, um ambiente de aprendizado e desenvolvimento assistido por IA. Este repositório não contém apenas código, mas a "mente" e as regras de um Agente Inteligente configurado para ser seu professor particular e colega de programação (pair programming).

---

## 🧠 O que é um Agente?
Diferente de um chatbot tradicional em que você precisa copiar e colar código o tempo todo, um **Agente** é uma Inteligência Artificial integrada diretamente ao seu ambiente de desenvolvimento (IDEs, como o VS Code). Ele consegue "enxergar" o contexto do seu projeto, ler seus arquivos, propor edições visuais e executar tarefas utilizando ferramentas próprias, tudo de forma autônoma, mas sempre sob o seu controle.

## ⚙️ Como um Agente funciona?
O agente ganha vida através da combinação do seu motor de IA com uma estrutura de regras rigorosa. Em vez de agir como um gerador de código genérico, ele opera em camadas:

* **Regras Globais (`GEMINI.md`):** É a "constituição" do workspace. Localizado na raiz do projeto, este arquivo dita os comportamentos e valores inegociáveis do agente (ex: "priorize o aprendizado", "nunca altere um arquivo silenciosamente").
* **Skills (`.agents/skills/`):** São manuais de operação especializados. Enquanto as regras globais dizem *como se comportar*, as skills ensinam o passo a passo de *o que fazer* em tarefas específicas.
* **Ferramentas (Tools):** As capacidades que o agente tem de ler arquivos, comparar versões de código (Diff) e interagir com o projeto.

## 🎯 O que o MEU agente faz?
O **TutorProgramacao** foi desenhado com o propósito de evitar a perda de contexto e a dependência cega da IA. Ele possui 4 habilidades principais devidamente mapeadas em suas *Skills*:

1. **Programming Teacher:** Ensina conceitos novos usando a pedagogia de um tutor Socrático. Utiliza uma "Escada de Dicas" progressiva e exemplos executáveis, recusando-se a entregar respostas prontas para estimular o raciocínio.
2. **Code Review:** Avalia códigos de forma não-destrutiva. Explica a lógica em camadas (o que faz, por que foi feito assim, como funciona) e ativa um "Radar de Casos Extremos" para encontrar vulnerabilidades lógicas.
3. **Debugging Tutor:** Em caso de bugs (como um *NullPointerException*), atua como um parceiro de investigação. Ajuda a isolar a causa raiz e testar hipóteses, garantindo que o programador entenda o erro antes de corrigi-lo.
4. **Code Editing:** Refatora e altera arquivos de forma extremamente segura. Mapeia o impacto da mudança, aplica o código em etapas lógicas e exige a aprovação explícita (Accept/Decline) do programador visualizando o Antes/Depois.

## 🚀 Como montar seu agente a partir do meu
Para reutilizar este segundo cérebro em seus próprios projetos, a arquitetura é totalmente portátil:

1. **Use este Template:** Clique no botão verde **`Use this template`** (se estiver no GitHub) para criar um novo repositório espelhando toda essa estrutura de diretórios e regras.
2. **Clone o Repositório:** Baixe o projeto recém-criado para a sua máquina local.
3. **Prepare seu Editor:** Utilize o VS Code com a sua extensão de Agente de IA configurada (como o Google Antigravity ou equivalente com suporte a Gemini).
4. **Abra o Projeto:** Ao abrir a pasta no VS Code, o agente mapeará automaticamente o arquivo `GEMINI.md` e a pasta `.agents`. Ele assumirá instantaneamente a personalidade do TutorProgramacao.
5. **Adapte e Evolua:** Assim que clonar, o repositório é seu! Sinta-se livre para adicionar novas pastas dentro de `skills` ou alterar as regras globais para que a IA se comporte exatamente da maneira que o seu novo projeto exigir.

### Caso queira contribuir só mandar um Pull Request (PR)!!!

