# 📊 Dashboard de Performance - Google Ads
### Tráfego Pago • Climatização • Análise de KPIs

---

## 📌 Visão Geral

Este projeto consiste no desenvolvimento de um dashboard no Power BI para análise estratégica de campanhas de tráfego pago (Google Ads) no setor de climatização. 

O objetivo principal é centralizar as métricas de performance em uma única solução visual, permitindo ao gestor otimizar os investimentos, acompanhar os resultados em tempo real e tomar decisões baseadas em dados sem depender de relatórios estáticos em PDF.

---

## 🏗️ Estrutura e Preparação dos Dados (ETL)

O fluxo de dados foi desenhado para eliminar processos manuais:

- **Conectividade:** Integração com o Google Ads utilizando a extensão **SyncWith** para Google Sheets, alimentando o modelo de forma automatizada.
- **Tratamento de Dados (Power Query):** Aplicação de etapas de limpeza, tipagem correta de dados e desduplicação para garantir a integridade das informações no painel.

---

## ⚠️ Desafios Técnicos e Limitações da API

Durante o desenvolvimento, o projeto enfrentou restrições severas impostas pela API de extração e pelas políticas da plataforma:

- **Dimensões Prejudicadas (Dados Geográficos e Demográficos):** Devido a limitações na conexão e extração via API, não foi possível carregar os dados de localidade (geográficos) e perfil demográfico (como gênero e idade), restringindo a análise a métricas puramente técnicas de campanha.
- **Quebra do Modelo Star Schema (Ad Groups):** A API não permitiu unificar a dimensão de Grupos de Anúncios (*Ad Groups*) junto à tabela de campanhas de forma consistente. Por conta dessa limitação na estrutura dos dados extraídos, não foi possível consolidar um modelo puramente *Star Schema*.

---

## 📊 Análise do Dashboard e Insights de Negócio

O projeto é composto por uma tela centralizada focada no acompanhamento dos principais indicadores do negócio:

| Indicadores e Performance | Visualização do Painel |
| :--- | :--- |
| **Definição de KPIs de Mercado:**<br>• Monitoramento de metas como CTR ideal (acima de 5%) e Taxa de Conversão de Página (acima de 12%).<br>• Alinhamento do Custo por Lead (CPL) com base no Ticket Médio dos serviços.<br><br>**Análise de Sazonalidade:**<br>• Identificação de que os meses de alta temporada (Verão - Janeiro e Fevereiro) geram maior volume bruto de leads e menor custo por clique (CPC) devido à urgência do mercado local, mesmo apresentando taxas percentuais (CTR) menores que os meses frios. | <img src="https://github.com/KathAlmeida/GoogleADS_Portf-lio/blob/main/IMAGES/image.jpg?raw=true" width="450"> |

---

## 💡 Próximos Passos (Processo Comercial)

Como oportunidade de evolução para o projeto, está planejada a integração de uma planilha simplificada de fechamentos comerciais. O objetivo é cruzar os dados de Marketing com as Vendas reais para calcular a conversão final de leads em contratos e mensurar o ROI real do negócio.

---

## 🛠️ Ferramentas Utilizadas

- **Google Ads** (Fonte de dados)
- **Google Sheets & SyncWith** (Extração e Automação)
- **Power BI & Power Query** (Tratamento e Visualização)

---

## 🔗 Links Úteis

- [Visualizar Dashboard Interativo](https://app.powerbi.com/view?r=eyJrIjoiM2JjZGQ2YzktNTJiMC00OWEzLWEyMGItNzA2MGQzODc1YTYzIiwidCI6IjcyNGM3NWE1LTZkM2MtNDdmNy1hMmVhLWZkODdmOTg3MDM3NSJ9)


---
