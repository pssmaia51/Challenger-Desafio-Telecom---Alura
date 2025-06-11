# 📊 Análise de Evasão de Clientes – Telecom X

## 🎯 Objetivo

A Telecom X vem enfrentando uma taxa crescente de evasão de clientes (churn). Este relatório documenta o processo de ETL (Extração, Transformação e Carga) e a Análise Exploratória de Dados (EDA) realizada sobre os dados dos clientes com o objetivo de identificar padrões de comportamento que possam explicar o churn.

---

## 🔍 ETL – Extração, Transformação e Carga

### 🔹 Extração

Os dados foram extraídos de um arquivo JSON com estrutura aninhada. Utilizou-se a biblioteca `json` em conjunto com `pandas.json_normalize` para converter os dados em um DataFrame tabular.

### 🔹 Transformação

As principais etapas foram:

- **Normalização dos dados aninhados** com `pd.json_normalize`
- **Conversão de colunas numéricas** (ex.: `account_Charges_Total`, `account_Charges_Monthly`)
- **Tratamento de valores faltantes e tipos de dados**
- **Padronização de nomes de colunas** para facilitar o manuseio

### 📊 EDA – Análise Exploratória de Dados
1. Distribuição de Clientes por Churn
A maioria dos clientes ainda permanece, mas a quantidade de cancelamentos é significativa:
Churn = No: clientes ativos
Churn = Yes: clientes que cancelaram
2. Gasto Total vs Churn
Clientes que evadiram tendem a ter menor gasto total, o que pode indicar:

Baixo tempo de permanência
Menor engajamento com os serviços
3. Tempo de Contrato (Tenure) vs Churn
Clientes com menos meses de contrato apresentaram taxas de churn muito superiores.

Retenção aumenta proporcionalmente ao tempo de permanência.
4. Tipo de Contrato vs Churn
Contratos mensais ("Month-to-month") são os principais associados à evasão.

Contratos anuais e bienais mostram menor propensão ao churn.

### 📌 Conclusões
Clientes com baixo tempo de permanência e contratos mensais têm maior probabilidade de cancelar o serviço.

O gasto acumulado mais baixo entre os clientes que evadiram indica a necessidade de ações iniciais de retenção.

### 💡 Recomendações Estratégicas
Oferecer planos de fidelidade com benefícios progressivos para contratos anuais e bienais.

Criar campanhas de retenção focadas nos primeiros meses de contrato, onde o churn é mais crítico.

Analisar perfis de clientes com churn alto para ações segmentadas, como descontos personalizados ou canais de atendimento prioritário.

Monitorar o engajamento com os serviços (internet, suporte, faturas) para prever comportamentos de evasão.

