# Casos de Teste - Busca de Passagens Aéreas

## Busca Básica

| ID | Cenário | Pré-condição | Dados de Teste | Resultado Esperado | Resultado Obtido | Status | Prioridade |
|----|---------|--------------|----------------|---------------------|-------------------|--------|------------|
| CT-001 | Realizar busca válida entre origem e destino | Usuário na página inicial | Origem: São Paulo (Todos os Aeroportos) / Destino: Belo Horizonte (Todos os Aeroportos) | Sistema deve retornar a lista de resultados disponíveis para a rota | Resultados retornados corretamente para a rota informada | ✅ Passou | Alta |
| CT-002 | Realizar busca somente de ida | Usuário na página inicial | Selecionar opção "Somente ida" | Sistema deve ocultar o campo de data de volta e buscar normalmente | Comportamento correspondeu ao esperado | ✅ Passou | Média |
| CT-003 | Alterar número de passageiros | Usuário na página inicial | 2 adultos | Sistema deve manter a seleção e refletir no resumo da busca | Passageiro exibido corretamente no resumo | ✅ Passou | Média |

---

## Data e Horário

| ID | Cenário | Pré-condição | Dados de Teste | Resultado Esperado | Resultado Obtido | Status | Prioridade |
|----|---------|--------------|----------------|---------------------|-------------------|--------|------------|
| CT-004 | Selecionar data de ida e volta válidas | Usuário no campo de datas | Ida: 31/07/26 / Volta: 01/08/26 | Sistema deve aceitar e exibir as datas selecionadas | Datas aceitas e refletidas corretamente na busca | ✅ Passou | Alta |
| CT-005 | Selecionar data de ida e, em seguida, data de volta em sequência | Usuário no campo de datas | Clicar em "Ida" e depois em "Volta" rapidamente | Calendário anterior deve fechar antes de abrir o próximo, sem sobreposição visual | Os dois calendários (mês de ida e mês de volta) ficaram abertos e sobrepostos na tela simultaneamente | ⚠️ Passou com ressalva | Média |
| CT-006 | Selecionar data de volta anterior à data de ida | Usuário no campo de datas | Ida: 31/07/26 / tentativa de volta anterior | Sistema deve impedir a seleção de datas inconsistentes | Sistema não permitiu selecionar data de volta anterior à ida | ✅ Passou | Alta |

---

## Filtro de Preço

| ID | Cenário | Pré-condição | Dados de Teste | Resultado Esperado | Resultado Obtido | Status | Prioridade |
|----|---------|--------------|----------------|---------------------|-------------------|--------|------------|
| CT-007 | Aplicar filtro de preço dentro da faixa de valores disponível | Resultados de busca carregados | Ajustar slider de preço para um valor intermediário | Sistema deve atualizar a lista com resultados dentro da faixa | Resultados filtrados corretamente conforme faixa selecionada | ✅ Passou | Alta |
| CT-008 | Aplicar filtro de preço que não retorna nenhum resultado | Resultados de busca carregados | Ajustar valor máximo para abaixo do menor preço disponível (ex: R$ 123) | Sistema deve exibir mensagem informando ausência de resultados para o filtro | Mensagem "Não encontramos opções para o filtro selecionado" exibida corretamente | ✅ Passou | Alta |
| CT-009 | Clicar em "Limpar" no painel de filtros após tela sem resultados | Tela exibindo "Não encontramos opções para o filtro selecionado" | Clicar no botão "Limpar" (painel lateral) | Filtros devem ser resetados e resultados devem voltar a ser exibidos | Em novo teste, filtros foram resetados e resultados voltaram a ser exibidos corretamente | ✅ Passou | Alta |
| CT-010 | Clicar em "Limpe os filtros" na tela de ausência de resultados | Tela exibindo "Não encontramos opções para o filtro selecionado" | Clicar no botão "Limpe os filtros" (área central) | Filtros devem ser resetados e resultados devem voltar a ser exibidos | Em novo teste, comportamento ocorreu conforme esperado | ✅ Passou | Alta |

---

## Filtro de Paradas e Companhia

| ID | Cenário | Pré-condição | Dados de Teste | Resultado Esperado | Resultado Obtido | Status | Prioridade |
|----|---------|--------------|----------------|---------------------|-------------------|--------|------------|
| CT-011 | Selecionar filtro "Todas as paradas" | Resultados de busca carregados | Opção "Todas as paradas" marcada | Sistema deve manter todos os resultados disponíveis | Resultados mantidos corretamente | ✅ Passou | Média |
| CT-012 | Selecionar uma companhia aérea específica | Resultados de busca carregados | Selecionar apenas uma companhia (ex: LATAM) | Sistema deve exibir somente voos da companhia selecionada | Resultados filtrados corretamente pela companhia escolhida | ✅ Passou | Alta |
| CT-013 | Combinar filtro de companhia e filtro de preço simultaneamente | Resultados de busca carregados | Companhia + faixa de preço específica | Sistema deve aplicar ambos os filtros de forma combinada | Filtros combinados aplicados corretamente | ✅ Passou | Média |

---

## Navegação

| ID | Cenário | Pré-condição | Dados de Teste | Resultado Esperado | Resultado Obtido | Status | Prioridade |
|----|---------|--------------|----------------|---------------------|-------------------|--------|------------|
| CT-014 | Retornar para a página inicial a partir da tela de resultados | Usuário na tela de resultados de busca | Clicar em "Voltar para a página inicial" | Sistema deve redirecionar corretamente sem erros | Redirecionamento ocorreu corretamente | ✅ Passou | Baixa |

---

# Testes Exploratórios

## Charter 1 - Validação de Filtros

**Objetivo:** identificar inconsistências na aplicação e no reset dos filtros de busca.

Explorar:
- Combinações de filtros (preço + companhia + paradas);
- Valores extremos no filtro de preço;
- Comportamento ao não haver resultados para o filtro aplicado.

## Charter 2 - Experiência de Seleção de Datas

**Objetivo:** avaliar a usabilidade do componente de calendário na seleção de ida e volta.

Explorar:
- Sequência de cliques entre os campos de ida e volta;
- Sobreposição de elementos visuais;
- Navegação entre meses/anos no calendário.

## Charter 3 - Consistência entre Sessões

**Objetivo:** avaliar a persistência de filtros e dados durante a navegação.

Explorar:
- Retorno à página inicial e nova busca;
- Atualização da página durante uma busca filtrada.

---

# Registro de Achados

| ID | Tipo | Descrição | Severidade | Status |
|----|------|-----------|------------|--------|
| ACH-001 | Melhoria (UX) | Ao selecionar a data de ida e, em seguida, a data de volta em sequência, os dois calendários (referentes a meses diferentes) permanecem abertos e sobrepostos na tela, prejudicando a leitura das datas disponíveis. | Baixa-Média | Aberto |

*Observação: um comportamento de não reset do botão "Limpar filtros" foi observado em um primeiro momento (CT-009/CT-010), porém não se confirmou em execuções posteriores, sendo tratado como resultado aprovado após reteste.*
