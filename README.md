# Agent1-agent2

Sistema multiagente para criação de roadmaps personalizados de carreira em tecnologia.

## Visão Geral

Este projeto implementa dois agentes de IA que trabalham em conjunto para guiar profissionais em sua jornada de carreira em tecnologia:

| Agente   | Papel                            | Arquivo                         |
|----------|----------------------------------|---------------------------------|
| Agent 1  | Entrevistador de Perfil          | [`agents/agent1.md`](agents/agent1.md) |
| Agent 2  | Planejador de Carreira           | [`agents/agent2.md`](agents/agent2.md) |

## Fluxo do Sistema

```
Usuário → Agent 1 (Entrevistador) → Agent 2 (Planejador) → Plano Personalizado
```

1. **Agent 1** conduz uma entrevista conversacional e coleta o perfil do usuário.
2. **Agent 1** envia os dados estruturados ao **Agent 2** via payload JSON.
3. **Agent 2** gera um plano completo de carreira personalizado em 120 dias.

## Dados Coletados pelo Agent 1

```json
{
  "CARREIRA_ESCOLHIDA": "QA Automatizador",
  "HORAS_SEMANA": "10",
  "EXPERIENCIA": "iniciante",
  "OBJETIVO": "primeiro emprego",
  "PREFERENCIA": "código",
  "INTERESSES": "Java, Selenium, Postman"
}
```

## Plano Gerado pelo Agent 2

O Agent 2 gera um plano completo contendo:

- 🧩 **Visão do dia a dia** — como é a rotina profissional da carreira escolhida
- 🧠 **Mapa de skills** — core skills, nice-to-have e ferramentas
- 📅 **Roadmap de 120 dias** — dividido em 4 meses com metas semanais
- 🚀 **Projeto de portfólio** — escopo, entregáveis e critérios de aceitação
- 💬 **Roteiro de entrevistas** — perguntas comuns e como respondê-las
- 🎓 **Trilha DIO recomendada** — bootcamp alinhado à carreira

## Foco das Carreiras

O sistema foi especialmente desenvolvido para carreiras de **Qualidade de Software**:

- QA Manual
- QA Automatizador (Java, Selenium, Cucumber, Robot)
- QA de API (Postman, Swagger, SoapUI)
- QA com IA (testes inteligentes, automação assistida por IA)
- QA de Performance
- QA Full Stack

## Como Usar

1. Configure o **Agent 1** com o prompt em [`agents/agent1.md`](agents/agent1.md).
2. Configure o **Agent 2** com o prompt em [`agents/agent2.md`](agents/agent2.md).
3. Conecte os dois agentes para que o Agent 1 envie o payload JSON ao Agent 2.
4. Inicie uma conversa com o Agent 1 — ele conduzirá a entrevista e acionará o Agent 2 automaticamente.
