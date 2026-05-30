# 💄 Power BI Analytics: E-commerce de Cosméticos (Mercado Indiano)

Este repositório contém um projeto de **Business Intelligence (BI)** desenvolvido no Power BI, baseado em um conjunto de dados reais de um e-commerce indiano especializado em produtos de estética e cosméticos (foco em variações de óleos labiais, gloss e maquiagens).

O objetivo principal deste projeto foi realizar o processo completo de engenharia e análise de dados: extração, limpeza/transformação via **Power Query**, modelagem de dados e criação de um **Painel Gerencial** estratégico para tomada de decisões executivas.

---

## 📊 O Dashboard (Painel Gerencial)

O painel foi estruturado para fornecer uma visão clara sobre saúde financeira, eficiência operacional, comportamento de pagamento e sazonalidade das vendas. Todos os valores originais foram cotados e normalizados em **Dólar ($)**.

### 1. Métricas Principais (KPIs)
* **Faturamento Total:** `$8,52 Mil` — Volume bruto de vendas gerado no período.
* **Custo de Desconto:** `$5,70 Mil (66,9%)` — Revela uma estratégia comercial agressiva baseada em promoções e cupons, consumindo uma parcela significativa do faturamento.
* **Custo de Frete:** `$558,54` — Custos logísticos acumulados de entrega.
* **Lucro Total:** `$2,26 Mil (Margem de 26,5%)` — O ganho líquido real da operação após a dedução de descontos e custos logísticos.
* **Ticket Médio:** `$36,88` — O valor médio gasto por cliente em cada transação.

### 2. Visões Analíticas Incorporadas
* **Quantidade de Transações por Operação (Meios de Pagamento):** Mostra um equilíbrio quase perfeito entre o gateway online **Razorpay (442 transações)** e pedidos via **Dinheiro em espécie (434 transações)** (antigo *Offline Payments*).
* **Status de Transações:** Demonstra alta estabilidade na operação com **97,03% de sucesso**, contra 2,85% de recusas e uma parcela mínima de estornos.
* **Volumetria de Vendas por Ano/Mês (2021):** Linha temporal identificando forte sazonalidade com picos acentuados de vendas nos meses de **Maio (160 transações)** e **Julho (171 transações)**, auxiliando o planejamento de estoque futuros.
* **Top 5 Itens Mais Vendidos:** Detalhamento granular de performance de produto, revelando que a linha *24K rose Lip Oil Gloss* e suas respectivas variações de aplicadores (*Big doe wand*, *Sample Gloss*, *Cylindrical Tube*) lideram o volume de vendas da empresa.

---

## 🛠️ Processo de Tratamento de Dados (ETL)

O maior desafio técnico do projeto residiu na limpeza e padronização da base de dados bruta dentro do **Power Query**:

1. **Padronização de Gateway de Terceiros:** A base de dados trazia registros de vendas físicas ou na entrega classificados originalmente como `Offline Payments`. Para tornar o painel intuitivo e aderente à realidade do negócio, o termo foi tratado e substituído por `Dinheiro em espécie`.
2. **Análise de Variações de SKU:** Os produtos possuíam descrições longas contendo parâmetros de seleção (ex: `Select an Option:Sample Gloss`). Foi realizada a separação e tratamento textual para permitir tanto a análise macro do produto quanto a análise micro por variação de embalagem/aplicador.
3. **Tratamento de Localização (Desafio de Compliance):** Devido a políticas corporativas rígidas de segurança de dados territoriais impostas por redes institucionais e servidores Azure, os visuais geográficos padrão foram substituídos estrategicamente por visuais de barras de alta densidade e matrizes, garantindo a continuidade da análise regional sem violação de conformidade de infraestrutura.

---

## 🚀 Tecnologias Utilizadas

* **Power BI Desktop** — Modelagem, cálculos e design de interface.
* **Power Query (M Language)** — Extração, limpeza de strings, substituição de valores e ETL.
* **DAX (Data Analysis Expressions)** — Criação de medidas calculadas de margem de lucro, ticket médio e agrupamentos operacionais.

---

## 📂 Como Visualizar o Projeto

1. Certifique-se de ter o **Power BI Desktop** instalado em sua máquina.
2. Baixe o arquivo `.pbix` disponível neste repositório.
3. Abra o arquivo para interagir com os filtros de status, meios de pagamento e linhas de produtos.

---
*Projeto desenvolvido para fins de estudo e portfólio de Data Analytics.*

<img width="1024" height="531" alt="image" src="https://github.com/user-attachments/assets/9ebe860f-2ec2-4d88-95c3-9363c6713134" />

