# 🚀 Analisar Performance de Relatórios

O desempenho de um relatório impacta diretamente a experiência do usuário e pode influenciar o tempo de carregamento de cada visual no Power BI. Este módulo apresenta as práticas essenciais para identificar e resolver gargalos de performance.

---

## 🔹 Performance Analyzer

A ferramenta **Performance Analyzer** permite medir:

- Tempo de renderização do visual  
- Tempo de execução de DAX  
- Tempo de consulta à fonte  
- Fatores que contribuem para lentidão  

### ✔ Como utilizar
1. Acesse: **View → Performance Analyzer**  
2. Clique em **Start recording**  
3. Interaja com os visuais  
4. Avalie o tempo gasto por cada componente  
5. Acesse detalhes e copie a consulta DAX se necessário  

---

## 🔹 Otimização de DAX

Recomendações gerais:

### ✔ Usar variáveis (VAR)
Melhora legibilidade e evita cálculos repetidos.

```DAX
Total Com Desconto =
VAR vBase = [Total Vendas]
RETURN vBase * 0.9
```

### ✔ Evitar FILTER sobre tabelas grandes
Sempre que possível filtrar colunas, não tabelas.

```DAX
-- Evitar
CALCULATE([Total Vendas], FILTER(FatoVendas, FatoVendas[Categoria] = "A"))

-- Preferir
CALCULATE([Total Vendas], FatoVendas[Categoria] = "A")
```

### ✔ Evitar funções iterativas desnecessárias  
Ex.: SUMX sobre tabelas muito grandes quando SUM simples resolve.

---

## 🔹 Otimizar o Layout e a Página do Relatório

### ✔ Reduzir número de visuais
Acima de **20 visuais em uma mesma página**, o desempenho normalmente cai.

### ✔ Minimizar segmentadores
Segmentadores (especially dropdowns complexos) consomem muita memória.

### ✔ Reduzir elementos gráficos pesados
- Imagens pesadas  
- Mapas detalhados  
- Visualizações customizadas mal otimizadas  

---

## 🔹 Melhorar Consultas e Interações

- Desativar interações desnecessárias entre visuais  
- Usar botões no lugar de muitos segmentadores  
- Substituir joins complexos feitos em DAX por modelagem melhorada  
- Usar agregações para tabelas grandes (Premium ou otimização avançada)  

---

## 🔹 Boas Práticas Adicionais

### ✔ Usar medidas em vez de colunas calculadas  
Medidas são mais leves e calculadas sob demanda.

### ✔ Ajustar cardinalidade  
Menos valores distintos = melhor compressão e performance.

### ✔ Evitar *bidirectional relationships*  
Usar apenas quando absolutamente necessário.

---

## 📚 Links Oficiais

- Power BI Performance Best Practices:  
  https://learn.microsoft.com/power-bi/guidance/power-bi-performance-best-practices

---

Este material resume as principais técnicas de diagnóstico e otimização de desempenho, fundamentais para a certificação PL-300 e para criação de relatórios de alta performance no Power BI.
