# 🏗️ Design de Modelo de Dados

Este módulo aprofunda conceitos de **modelagem dimensional**, essenciais para o desempenho e clareza do modelo no Power BI.

---

## 🔹 Modelo Estrela (Star Schema)

A estrutura recomendada pela Microsoft para BI:

- **Tabela Fato** → transações, valores numéricos, chaves estrangeiras  
- **Tabelas Dimensão** → contexto, atributos, categorias  
- **Relacionamentos 1:* (um para muitos)**  

Benefícios:

- Melhor compressão de dados  
- Menor complexidade  
- Melhor desempenho em DAX  
- Melhor uso de agregações  

---

## 🔹 Tabela Fato – características

- Alta granularidade  
- Muitas linhas  
- Poucas colunas  
- Colunas numéricas e chaves  

Exemplos:

- Fato Vendas  
- Fato Estoque  
- Fato Transações  

---

## 🔹 Tabelas Dimensão – características

- Muitas colunas  
- Poucas linhas  
- Atributos descritivos  
- Hierarquias (Ano > Mês > Dia, Região > Estado > Cidade)  

---

## 🔹 Tipos de Cardinalidade

| Tipo | Uso |
|------|-----|
| **1:* (um para muitos)** | padrão ideal |
| ***:1 (muitos para um)** | equivalente ao 1:* invertido |
| ***:* (muitos para muitos)** | apenas quando necessário |

---

## 🔹 Direção de Filtro

| Direção | Descrição |
|---------|-----------|
| **Single** | ideal, mais eficiente |
| **Both** | usar com cautela, pode causar loops |

---

## 🔹 Relacionamentos Ativos e Inativos

- **Ativo** → usado por padrão  
- **Inativo** → habilitado via `USERELATIONSHIP()`  

Exemplo:

```DAX
Vendas Ano Fiscal =
CALCULATE(
    [Total Vendas],
    USERELATIONSHIP(DimCalendario[AnoFiscal], FatoVendas[Data])
)
```

---

## 🔹 Tabelas de Datas

Requisitos:

- Coluna contínua (sem buracos)  
- Sem horários  
- Cobrir todo o intervalo do dataset  
- Marcar como **Date Table**  

---

## 📚 Links Oficiais

- Star Schema: https://learn.microsoft.com/power-bi/guidance/star-schema  
- Relationships: https://learn.microsoft.com/power-bi/transform-model/desktop-relationships  
