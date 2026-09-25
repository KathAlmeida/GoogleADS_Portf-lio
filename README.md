# 📊 Dashboard de Performance - Google Ads

### Tráfego Pago • Climatização • Análise de KPIs

---

## 📌 Visão Geral

Este projeto consiste no desenvolvimento de um dashboard no Power BI para análise estratégica de campanhas de tráfego pago (Google Ads) no setor de climatização.

O objetivo principal é centralizar as métricas de performance em uma única solução visual, permitindo ao gestor otimizar os investimentos, acompanhar os resultados em tempo real e tomar decisões baseadas em dados sem depender de relatórios estáticos em PDF.

**Período analisado:** agosto/2025 a maio/2026
**Resultados consolidados no período:** R$ 8.534 investidos, 553 leads gerados, CPL médio de R$ 15, CTR de 9%, CPC médio de R$ 4 e taxa de conversão de página de 28%.

---

## 🏗️ Estrutura e Preparação dos Dados (ETL)

O fluxo de dados foi desenhado para eliminar processos manuais:

- **Conectividade:** Integração com o Google Ads utilizando a extensão **SyncWith** para Google Sheets, alimentando o modelo de forma automatizada.
- **Tratamento de Dados (Power Query):** Aplicação de etapas de limpeza, tipagem correta de dados e desduplicação para garantir a integridade das informações no painel.

---

## ⚠️ Desafios Técnicos e Limitações da API

Durante o desenvolvimento, o projeto enfrentou restrições impostas pela API de extração e pelas políticas da plataforma:

- **Dimensões Prejudicadas (Dados Geográficos e Demográficos):** Devido a limitações na conexão e extração via API, não foi possível carregar os dados de localidade (geográficos) e perfil demográfico (como gênero e idade), restringindo a análise a métricas puramente técnicas de campanha.
- **Quebra do Modelo Star Schema (Ad Groups):** A API não permitiu unificar a dimensão de Grupos de Anúncios (*Ad Groups*) junto à tabela de campanhas de forma consistente. Por conta dessa limitação na estrutura dos dados extraídos, não foi possível consolidar um modelo puramente *Star Schema*.

---

## 📊 Análise do Dashboard e Insights de Negócio

![Dashboard - Análise de Campanhas de Geração de Leads](https://github.com/KathAlmeida/GoogleADS_Portf-lio/raw/main/IMAGES/image.jpg?raw=true)

### 1. Sazonalidade domina o volume de leads — não o orçamento

O volume de leads saltou de **13 em agosto/25 para um pico de 126 em janeiro/26**, coincidindo com o verão — período de alta demanda por climatização. A partir de fevereiro, o volume caiu de forma consistente (62 → 72 → 67 → 14 em maio), **mesmo com o investimento subindo** de R$ 745 (fev) para R$ 1.540 (abr).

Essa inversão (mais gasto, menos leads) evidencia que o problema não era orçamento, e sim demanda de mercado: no inverno, a procura por climatização cai naturalmente, e nenhum aumento de investimento reverte isso de forma eficiente.

**Decisão recomendada:** reduzir o aporte de mídia nos meses de baixa temporada (outono/inverno) e concentrar o orçamento nos meses de alta sazonalidade, onde o retorno por real investido é comprovadamente maior.

### 2. Funil de conversão: mais eficiente do que parece à primeira vista

Do total de **~23 milhões de impressões** no período, **8,53%** resultaram em cliques. Desse volume de cliques, **27,72%** converteram em leads que efetivamente chegaram ao time comercial — uma taxa de conversão de clique-para-lead considerada alta, o que indica boa aderência entre anúncio, página de destino e proposta de valor.

Ainda assim, existe espaço para reduzir desperdício de verba: uma segmentação mais refinada do público-alvo tende a elevar a taxa de cliques (hoje em 8,53%) sem perder a qualidade de conversão já observada.

### 3. CTR alto nem sempre significa CPC baixo

É comum a crença de que quanto maior o CTR, menor será o custo por clique. Os dados do período **não sustentam essa correlação direta**:

| Mês | CPC | CTR |
|---|---|---|
| Ago/25 | R$ 13,59 | 7% |
| Fev/26 | R$ 3,61 | 11% |

Fevereiro teve o CTR mais alto do período (11%) *e* um dos CPCs mais baixos (R$ 3,61), mas outros meses com CTR parecido não repetiram esse padrão de custo. Isso mostra que o CPC responde a outras variáveis (concorrência no leilão, qualidade do anúncio, sazonalidade de demanda) além do CTR isoladamente — uma heurística simplista de "só melhorar o CTR" não garante redução de custo.

---

## 💡 Próximos Passos (Processo Comercial)

- **Integração com CRM:** cruzar os dados de marketing com uma planilha simplificada de fechamentos comerciais, para calcular a conversão final de leads em contratos e mensurar o ROI real do negócio (hoje o dashboard mede geração de lead, não fechamento de venda — e o ticket médio varia por tipo de serviço).
- **Estratégias para baixa temporada:** desenhar campanhas ou ofertas específicas para os meses de menor demanda, já que reduzir investimento sem alternativa comercial deixa a operação ociosa nesse período.
- **Aprofundar a taxa de cliques (8,53%):** investigar se está dentro do esperado para o setor e testar segmentações mais específicas de público.

---

## 🛠️ Ferramentas Utilizadas

- **Google Ads** (Fonte de dados)
- **Google Sheets & SyncWith** (Extração e Automação)
- **Power BI & Power Query** (Tratamento e Visualização)

---

## 🔗 Links Úteis

- [Visualizar Dashboard Interativo](https://app.powerbi.com/view?r=eyJrIjoiM2JjZGQ2YzktNTJiMC00OWEzLWEyMGItNzA2MGQzODc1YTYzIiwidCI6IjcyNGM3NWE1LTZkM2MtNDdmNy1hMmVhLWZkODdmOTg3MDM3NSJ9)
