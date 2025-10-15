# 🧠 Análise de Prescritores — Segmentação, Retenção e Oportunidades de Mercado

Este projeto tem como objetivo realizar uma **análise exploratória e estratégica de prescritores**, identificando padrões de comportamento, níveis de engajamento e oportunidades de crescimento por região, especialidade e perfil de relacionamento.

A base de dados contém informações como:
- Nome do Prescritor  
- Especialidade  
- Região  
- Datas de início e última prescrição  
- Receita total e número de prescrições  
- Participação em eventos  
- Taxa média de abertura de mailmarketing (%)  
- Grau de satisfação (1–5)  
- Fonte de aquisição  

---

## 🧾 Objetivos da Análise

1. **Mensurar relacionamento e engajamento**
   - Tempo médio de relacionamento (em meses)
   - Identificação de prescritores ativos vs. inativos  
     *(Critério: mais de 90 dias sem prescrever = inativo)*
   - Cálculo da taxa de retenção (ativos / total)

2. **Avaliar desempenho financeiro**
   - Cálculo do **ticket médio por prescrição**
   - Análise de **receita média por região e especialidade**

3. **Identificar oportunidades de mercado**
   - Regiões e especialidades com **alta receita média, mas baixa participação**
   - Fontes de aquisição com melhor desempenho
   - Correlação entre satisfação, taxa de abertura e atividade

4. **Segmentar prescritores para estratégias de relacionamento**
   - Classificação de taxa de abertura (%) em 5 faixas
   - Criação de faixas de ticket médio com base no boxplot (quartis)
   - Cálculo do **Information Value (IV)** para identificar variáveis mais relevantes à inatividade

---

## 🧮 Principais Fórmulas Utilizadas

| Indicador | Fórmula | Descrição |
|------------|----------|-----------|
| Tempo de Relacionamento | `=ARREDONDAR.PARA.BAIXO((Data Última Prescrição-Data de Início)/30;0)` | Tempo médio em meses |
| Ticket Médio | `=[Receita Total] / [Total de Prescrições]` | Valor médio por prescrição |
| Status Ativo/Inativo | `=SE(HOJE() - [Data Última Prescrição] > 90; "Inativo"; "Ativo")` | Define status |
| Taxa de Retenção | `=Qtd_Ativos / Qtd_Total` | Percentual de prescritores ativos |
| IV | `SOMATÓRIO((Dist_Good - Dist_Bad) * LN(Dist_Good / Dist_Bad))` | Information Value |

---

## 📈 Gráficos e Visualizações

O arquivo em Excel contém os seguintes painéis:

- 🥧 **% de Inativos** (Gráfico de Pizza)  
- 📊 **Receita por Região** (Barras)  
- 📉 **Valor médio de receita e média de prescrições por especialidade** (Colunas)  
- 📈 **Captação de Prescritores por Mês** (Linha)  
- 📊 **Distribuição por Fonte de Aquisição** (Coluna)  
- 🧩 **Participação em Eventos** (Coluna)  
- 💬 **Prescritores por Nível de Satisfação** (Coluna)  
- 🧠 **Prescritores por Especialidade** (Coluna)  

---

![Imagem-gráfico](/img-github.png)

---

## 🔍 Resultados e Insights

### 1. **Atividade e Retenção**
- Tempo médio de relacionamento: **X meses**  
- Taxa de retenção: **Y%**  
- Maior concentração de inativos observada em prescritores com baixa taxa de abertura e menor satisfação.

### 2. **Análise de Information Value (IV)**  
| Variável | IV | Interpretação |
|-----------|----|---------------|
| Participou de Eventos | 0,00 | Irrelevante |
| Fonte de Aquisição | 0,05 | Fraca |
| Grau de Satisfação | 0,08 | Fraca |
| Especialidade | 0,05 | Fraca |
| Faixa Taxa de Abertura (%) | 0,03 | Fraca |
| Faixa Ticket Médio | 0,08 | Fraca |
| Região | 0,03 | Fraca |
| Total de Prescrições | 0,02 | Irrelevante |
| Tempo de Relacionamento | 0,08 | Fraca |

**Interpretação:**  
As variáveis **Grau de Satisfação**, **Ticket Médio** e **Tempo de Relacionamento** possuem maior poder preditivo sobre a inatividade e devem ser priorizadas em campanhas de retenção e reativação.

---

## 💡 Respostas às Questões Analíticas

### 🔹 Recuperação de Clientes
Os prescritores prioritários para reativação são aqueles com:
- Alto **ticket médio**
- Boa **satisfação**
- Longo **tempo de relacionamento**
Mesmo estando inativos, eles têm maior probabilidade de retorno e valor potencial maior.

---

### 🔹 Pesquisa de Produto e Satisfação
Selecionar prescritores com:
- **Níveis de satisfação extremos** (1 e 5) → para entender motivos de insatisfação e boas práticas.
- **Alta taxa de abertura (%)** → maior engajamento e melhor feedback qualitativo.
- **Participação ativa em eventos** → perfil colaborativo e aberto à inovação.

---

### 🔹 Oportunidades de Mercado
Identificadas regiões e especialidades com:
- **Alta receita média (ex: Sul –  R$ R$ 10.407,57)**  
- **Baixa participação na base de prescritores**
- **Nutricionista Funcional - Alta receita média R$ 12.128,20 e baixa participação 43 médicos**  
Essas áreas/especialidade representam **alto potencial de expansão**, sugerindo foco comercial e de relacionamento direcionado.

---

## 🧭 Ferramentas Utilizadas
- **Excel 2016**
  - Tabelas Dinâmicas  
  - Fórmulas estatísticas e lógicas  
  - Criação de gráficos e painéis  
  - Cálculo de Information Value (IV)
- **Power Query** para limpeza e padronização de dados  

---

## 📂 Link arquivo excel: 
[Inteligência de Mercado](/Estudo-de-Caso-Inteligencia-de-Mercado.xlsx)
---

Dúvidas, sugestões? Ficarei feliz em recebê-las


