# Plano de Testes

## Informações Gerais

| Item | Valor |
|------|--------|
| Projeto | QA Case Study - 123Milhas |
| Módulo | Busca de Passagens Aéreas (Filtros e Datas) |
| Responsável | Mateus Felipe dos Santos |
| Versão | 1.0 |
| Data | 31/07/2026 |

---

# Objetivo

Avaliar o comportamento da funcionalidade de busca de passagens aéreas da plataforma 123Milhas, com foco na aplicação de filtros de resultado (preço, paradas, companhia) e na seleção de datas de ida e volta, verificando regras de negócio, validações e consistência da experiência do usuário.

---

# Escopo

## Funcionalidades contempladas
- Busca de passagens (origem, destino, datas, passageiros)
- Filtro de preço por adulto
- Filtro de paradas
- Filtro de companhia aérea
- Seleção de datas de ida e volta (calendário)
- Botão "Limpar filtros"
- Navegação e persistência dos filtros aplicados

## Fora do escopo
- Fluxo de pagamento e checkout
- Cadastro e login de usuário
- Emissão de bilhetes
- Programa de milhas / Conexão123
- APIs e integrações externas
- Testes de performance e carga
- Testes de segurança

---

# Estratégia de Testes

Serão utilizados os seguintes tipos de teste:

- Testes Funcionais
- Testes Exploratórios
- Testes de Validação de Campos e Filtros
- Testes de Usabilidade (UX)
- Testes de Navegação

Os cenários serão priorizados considerando impacto na experiência do usuário e frequência de uso da funcionalidade (a busca e os filtros são o núcleo do produto).

---

# Ambiente

| Item | Valor |
|------|--------|
| Sistema Operacional | Windows 11 |
| Navegador | Brave |
| Ambiente | Ambiente público disponível ao usuário |
| URL | https://www.123milhas.com/ |

---

# Critérios de Entrada

- Acesso público à plataforma, sem necessidade de login.
- Conexão com internet disponível.
- Rota de busca definida (origem e destino válidos).

---

# Critérios de Saída

O módulo será considerado validado quando:

- Todos os casos de teste planejados forem executados.
- Os achados (bugs e melhorias) estiverem documentados e classificados.
- As evidências (prints e vídeo) estiverem anexadas.

---

# Riscos

| Risco | Impacto | Prioridade |
|--------|----------|------------|
| Filtros não retornarem resultados corretos | Alto | Alta |
| Botão "Limpar filtros" não resetar a busca | Alto | Alta |
| Datas inconsistentes serem aceitas (volta antes da ida, etc.) | Alto | Alta |
| Sobreposição visual entre elementos de UI (ex: calendários) | Médio | Média |
| Filtros combinados gerarem resultado inesperado | Médio | Média |

---

# Critérios de Priorização

Os testes serão executados seguindo a ordem:

1. Fluxo principal de busca
2. Validações de filtros (preço, paradas, companhia)
3. Cenários negativos (valores extremos, combinações inválidas)
4. Navegação e persistência (limpar filtros, voltar)
5. Usabilidade (calendário, responsividade dos componentes)

---

# Entregáveis

- Plano de Testes
- Casos de Teste
- Registro de Achados (bug)
