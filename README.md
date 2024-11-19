# 📊 **Análise do Impacto Social do aplicativo I’m Hungry!**

O **I’m Hungry!**, comprometido com eficiência operacional e impacto social, solicitou uma análise detalhada para mensurar os resultados de suas iniciativas sociais. Este estudo visou correlacionar o impacto dessas ações no ecossistema e no desempenho financeiro da empresa, fornecendo dados para embasar decisões estratégicas.

---

## 🛠 **Problema de Negócio**

**Como garantir que os investimentos feitos em iniciativas de impacto social resultem em melhorias tangíveis tanto para o ecossistema quanto para o desempenho financeiro?**  
Além disso, como mensurar e demonstrar claramente esse impacto às partes interessadas?

Para responder a essas questões, estruturamos o problema em cinco perguntas principais:

1. **Qual é o impacto das iniciativas sociais no volume de pedidos realizados no I’m Hungry!?**
2. **Qual o retorno financeiro gerado pelas iniciativas sociais?**
3. **Quais ações têm gerado maior engajamento entre consumidores e parceiros?**
4. **Como as iniciativas sociais influenciam a percepção da marca entre os consumidores?**
5. **Quais são os KPIs essenciais para avaliar a efetividade das iniciativas sociais?**

---

## 📋 **Modelo de Dados**

Foi desenvolvido um modelo de dados para sustentar a análise. Ele inclui as seguintes tabelas:

- **Iniciativas_Sociais:** Dados das ações realizadas (investimentos, localizações, descrição, etc.).
- **Pedidos:** Informações sobre os pedidos realizados, com vinculação às iniciativas sociais.
- **Engajamento:** Dados sobre a interação de consumidores e parceiros com as iniciativas.
- **Satisfacao:** Avaliações de satisfação (NPS e comentários).
- **Resultados_Financeiros:** Dados financeiros correlacionados às iniciativas sociais.
  
![Logo do GitHub](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*4GdBZ9-pzdFE-X6O_6PxZQ.jpeg)

[Acesse o Painel aqui](https://app.powerbi.com/view?r=eyJrIjoiNjg2MDllY2YtYjNlNi00OGM1LThhYzMtNDQzZjI2MzBkYzJiIiwidCI6IjgxY2RjMzU5LTkwYWQtNGJjOC1iNTUyLTNlZjI1NzBhY2ZkMyJ9)

---

## **Principais Insights**

### 1️⃣ **Impacto no Volume de Pedidos**
- **160 mil pedidos** foram realizados no período de iniciativas (jan-jun/2023), representando **53,3% do total anual**.
- Apenas **14% dos pedidos** nesse período estavam diretamente associados às iniciativas sociais, destacando uma **oportunidade para maior impacto direto**.

### 2️⃣ **Retorno Financeiro**
- **Investimento total:** R$ 128,9 milhões.  
- **Retorno financeiro:** R$ 101,41 milhões, resultando em um ROI de **-21,33%**.  
- **Ações com maior ROI:**
  - **Ação Verde:** ROI de **2629%**.
  - **Educando o Futuro:** ROI de **4373%**.

### 3️⃣ **Engajamento de Consumidores e Parceiros**
- **Comida para Todos** gerou o maior volume de pedidos: **19.210** (95,01% dos pedidos das campanhas).
- **Ação Verde:** 522 pedidos (2,58%).
- **Educando o Futuro:** 487 pedidos (2,41%).

### 4️⃣ **Percepção da Marca**
- **Comida para Todos** obteve o maior NPS médio (**8,3**) com **50,48% dos comentários avaliados como "bom"** e **49,09% como "excelente"**.
- Pedidos sem impacto social tiveram um NPS médio de **5,5**, destacando a diferença positiva causada pelas ações.

### 5️⃣ **KPIs Essenciais**
Foram definidos os seguintes KPIs para acompanhamento:
- **Volume de Pedidos:** Antes e durante as iniciativas.
- **Engajamento do Cliente:** Aderência por campanha.
- **Investimento por Iniciativa:** Controle de custos e ROI.
- **Satisfação (NPS):** Comparativo entre pedidos com e sem iniciativas.
- **Comentários do Cliente:** Classificação (bom, excelente, precisa melhorar).

---
### **Recomendações**
- **Marketing Direcionado**: Realizar campanhas mais agressivas para promover as iniciativas sociais, destacando os benefícios para a comunidade e o impacto gerado. Por exemplo, anúncios nas redes sociais que demonstrem como os pedidos estão ligados à melhoria social.
  
- **Incentivos Diretos**: Criar promoções ou recompensas para consumidores que participam de iniciativas sociais, como descontos ou brindes por meio de cupons ligados a ações específicas.
  
- **Parcerias Estratégicas**: Firmar parcerias com ONGs ou influenciadores para dar mais visibilidade às iniciativas e engajar consumidores emocionalmente.
  
- **Redirecionar Investimentos**: Concentrar esforços nas iniciativas com maior impacto financeiro e social (Ação Verde e Educando o Futuro). Reavaliar ou encerrar ações com baixo retorno, como “Comida para Todos”, caso o objetivo seja equilibrar impacto social e financeiro.
  
- **Campanhas Educativas**: Explicar claramente como essas iniciativas impactam o ecossistema. Exemplo: criar vídeos curtos que mostrem os resultados reais gerados pelas ações.
  
- **Engajamento Gamificado**: Implementar mecânicas de gamificação para consumidores e parceiros, como rankings ou recompensas baseadas no engajamento com iniciativas sociais.
  
- **Feedback Visível**: Exibir relatórios periódicos de impacto dentro do app para incentivar mais adesão. Ex.: “Você ajudou a plantar 100 árvores com seus pedidos!”.
  
- **Análise Geográfica**: Mapear quais regiões têm maior engajamento com as iniciativas e usar essa informação para direcionar campanhas mais localizadas.

---
## 🧮 **Fórmulas DAX Utilizadas**

```dax
%PedidosIniciativa = [PedidosIniciativas]/[Pedidosseminiciativas]
```
```dax
Contagem_Avaliacoes = 
COUNTROWS(
    FILTER(
        'Satisfacao',
        'Satisfacao'[Iniciativa_Associada] <> BLANK()
    )
)
```
```dax
Contagem_Avaliacoes = 
COUNTROWS(
    FILTER(
        'Satisfacao',
        'Satisfacao'[Iniciativa_Associada] <> BLANK()
    )
)
``````dax
Contagem_Avaliacoes = 
COUNTROWS(
    FILTER(
        'Satisfacao',
        'Satisfacao'[Iniciativa_Associada] <> BLANK()
    )
)
```
```dax
Custo_Por_Engajamento = 
DIVIDE(
    SUM(Iniciativas_Sociais[investimento]),
    [Engajamento_Por_Iniciativa]
)
```
```dax
Engajamento_Doacao = 
CALCULATE(
    COUNT(Engajamento[id_engajamento]),
    Engajamento[tipo_engajamento] = "Doação"
)
```
```dax
Engajamento_Feedback_Positivo = 
CALCULATE(
    COUNT(Engajamento[id_engajamento]),
    Engajamento[tipo_engajamento] = "Feedback Positivo"
)%PedidosIniciativa = [PedidosIniciativas]/[Pedidosseminiciativas]
```
```dax
Engajamento_Participacao = 
CALCULATE(
    COUNT(Engajamento[id_engajamento]),
    Engajamento[tipo_engajamento] = "Participação"
)
```
```dax
Engajamento_Por_Iniciativa = 
CALCULATE(
    COUNT(Engajamento[id_engajamento]),
    VALUES(Engajamento[id_iniciativa])
)
```
```dax
Iniciativatodas = COUNT(Iniciativas_Sociais[nome_iniciativa]) 
```
```dax
Investimento_Por_Engajamento = 
DIVIDE(
    SUM(Iniciativas_Sociais[investimento]),
    [Total_Engajamentos]
)
```

```dax
Lucro - investimento = [TotalRetornoFinanceiro]-[TotalInvestimento]  
```
```dax
Maior_Engajamento_Iniciativa = 
MAXX(
    SUMMARIZE(
        Engajamento,
        Engajamento[id_iniciativa],
        "Total_Engajamento", COUNT(Engajamento[id_engajamento])
    ),
    [Total_Engajamento]
)o]  
```
```dax
NPS_Medio_Por_Iniciativa = 
AVERAGEX(
    FILTER(
        'Satisfacao',
        'Satisfacao'[Iniciativa_Associada] <> BLANK()
    ),
    'Satisfacao'[Nps]
)
```
```dax
PedidosDuranteIniciativas = 
CALCULATE(
    [TotalPedidos],
    FILTER(
        Pedidos,
        Pedidos[Data_Pedido] >= DATE(2023, 1, 1) && 
        Pedidos[Data_Pedido] <= DATE(2023, 6, 15)
    )
)
```
```dax
PedidosIniciativas = COUNT(Iniciativas_Sociais[data_inicio]) 
```
```dax
Pedidosseminiciativas = [PedidosDuranteIniciativas]-[PedidosIniciativas] 
```
```dax
ROI = ([Lucro - investimento]/[TotalInvestimento])PedidosIniciativas] 
```
```dax
Total acumulado de Engajamento_Feedback_Positivo em id_iniciativa = 
CALCULATE(
	[Engajamento_Feedback_Positivo],
	FILTER(
		ALLSELECTED('Iniciativas_Sociais'[id_iniciativa]),
		ISONORAFTER('Iniciativas_Sociais'[id_iniciativa], MAX('Iniciativas_Sociais'[id_iniciativa]), DESC)
	)
)
```
```dax
Total acumulado de Engajamento_Feedback_Positivo em id_iniciativa 2 = 
CALCULATE(
	[Engajamento_Feedback_Positivo],
	FILTER(
		ALLSELECTED('Iniciativas_Sociais'[id_iniciativa]),
		ISONORAFTER('Iniciativas_Sociais'[id_iniciativa], MAX('Iniciativas_Sociais'[id_iniciativa]), DESC)
	)
)
```
```dax
Total_comentarios = COUNT(Satisfacao[comentario])
```
```dax
Total_Engajamentos = COUNT(Engajamento[id_engajamento])
```
```dax
TotalInvestimento = SUM(Iniciativas_Sociais[investimento])
```
```dax
TotalPedidos = COUNT(Pedidos[ID_Pedido])
```
```dax
TotalRetornoFinanceiro = SUM(Resultados_Financeiros[valor_resultado])
```
