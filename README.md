# 123milhas-qa-case-study# QA Case Study — 123Milhas

> Estudo de caso desenvolvido para demonstrar uma abordagem de Quality Assurance aplicada ao fluxo de busca de passagens da plataforma 123Milhas.

## Sobre o projeto

Este repositório apresenta um estudo de caso de QA realizado utilizando funcionalidades públicas da 123Milhas.

O objetivo foi aplicar técnicas de testes manuais em um cenário real, incluindo planejamento, execução de casos de teste, testes exploratórios e documentação de um bug encontrado durante a avaliação da experiência do usuário.

Todos os testes foram realizados utilizando funcionalidades públicas da plataforma. Este projeto possui finalidade exclusivamente educacional e de portfólio.

---

## Objetivos

- Elaborar um plano de testes.
- Criar casos de teste funcionais.
- Executar testes manuais e exploratórios.
- Identificar e documentar defeitos.
- Demonstrar organização e boas práticas em QA.

---

## Escopo

**Funcionalidade avaliada**

Busca de Passagens Aéreas.

**Incluído**

- Busca de passagens
- Seleção de datas
- Filtros de preço
- Filtros de paradas
- Filtros de companhia aérea
- Navegação entre resultados
- Validação do comportamento dos componentes de interface

**Fora do escopo**

- Login e cadastro
- Checkout e pagamento
- Emissão de passagens
- APIs e integrações
- Performance
- Segurança

---

## Estrutura do Projeto

```text
documentacao/
├── plano-de-testes.md
└── casos-de-teste.md

reporte-de-bugs/
└── BUG-001-calendarios-de-selecao-de-data-sao-exibidos-sobrepostos.md 

evidencias/
├── BUG-001-calendarios-selecao-data-sobrepostos.mp4
└── BUG-001-print.png

README.md
```

---

## Ferramentas

- Brave
- DevTools
- Git
- GitHub
- Markdown

---

## Resultados

| Métrica | Quantidade |
|---------|-----------:|
| Casos de teste planejados | 14 |
| Casos executados | 14 |
| Bugs encontrados | 1 |
| Bugs documentados | 1 |
| Sessões exploratórias | 1 |

---

## Bug encontrado

Durante a execução dos testes foi identificado um problema de usabilidade no componente de seleção de datas.

Ao abrir o calendário de ida e, em seguida, o de volta, ambos permanecem visíveis simultaneamente, ocasionando sobreposição dos componentes e prejudicando a interação do usuário.

O defeito foi reproduzido, documentado e acompanhado de evidências em vídeo.

---

## Aviso

Este projeto possui finalidade exclusivamente educacional e de portfólio.

Não possui qualquer vínculo ou afiliação com a 123Milhas. Todas as análises representam um estudo independente realizado em funcionalidades públicas da plataforma.
