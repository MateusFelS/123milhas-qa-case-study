# BUG-001 — Calendários de seleção de data são exibidos sobrepostos

## Informações

| Campo | Valor |
|-------|-------|
| ID | BUG-001 |
| Módulo | Busca de Passagens |
| Funcionalidade | Seleção de Datas |
| Severidade | Média |
| Prioridade | Média |
| Ambiente | Ambiente público disponível ao usuário |
| Navegador | Brave |
| Sistema Operacional | Windows 11 |
| Status | Aberto |

---

## Descrição

Ao abrir os seletores de data para alterar as datas de ida e volta, o sistema permite que mais de um calendário permaneça aberto simultaneamente, fazendo com que os componentes sejam exibidos sobrepostos e dificultem a interação do usuário.

---

## Pré-condições

- Usuário acessando a página de busca de passagens.
- Campos de data de ida e volta disponíveis para edição.

---

## Passos para reprodução

1. Acessar a página de busca de passagens.
2. Clicar no campo de data de ida para abrir o calendário.
3. Sem fechar o primeiro calendário, clicar no campo de data de volta.
4. Observar a exibição dos calendários.

---

## Resultado esperado

Ao abrir um calendário, qualquer outro calendário aberto deve ser fechado automaticamente, garantindo que apenas um seletor de datas permaneça visível por vez.

---

## Resultado obtido

Os calendários permanecem abertos simultaneamente e são exibidos sobrepostos, comprometendo a visualização e a usabilidade da interface.

---

## Impacto

A sobreposição dos calendários dificulta a seleção das datas, pode gerar cliques incorretos e prejudica a experiência do usuário durante a busca de passagens.

---

## Evidências

- Vídeo: [bug-001-calendarios-sobrepostos.mp4](../evidencias/bug-001-calendarios-sobrepostos.mp4)
- Print: ![Calendários sobrepostos](../evidencias/bug-001-print.png)
