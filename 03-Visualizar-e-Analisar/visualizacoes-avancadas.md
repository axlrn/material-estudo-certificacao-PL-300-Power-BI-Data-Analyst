# ⚙️ Visualizações Avançadas

Esta seção aprofunda recursos avançados para aprimorar storytelling e análise dentro do Power BI.

---

## 🔹 KPIs

KPIs destacam:
- Valor atual  
- Meta  
- Variação  
- Tendência  

Exemplo de medida:

```DAX
Meta Atingida = IF([Total Vendas] >= [Meta], "Sim", "Não")
```

---

## 🔹 Matriz (Matrix Visual)

Recursos:
- Stepped layout  
- Drilldown  
- Subtotais  
- Formatação condicional  
- Expandir/contrair níveis  

---

## 🔹 Gráficos de Combinação

Usos típicos:
- Coluna + linha  
- Dual axis  
- Mostrar valores e tendências simultaneamente  

---

## 🔹 Botões e Navegação

Tipos de botões:
- Navegação entre páginas  
- Bookmarks  
- Reset filters  
- Tooltip triggers  

---

## 🔹 Bookmarks

Permitem salvar estados do relatório:

- Filtros  
- Seleções  
- Visuais visíveis  
- Navegação  

---

## 🔹 Tooltips Personalizados

Podem conter:
- KPIs  
- Gráficos pequenos  
- Resumos de comparação  

---

## 🔹 Small Multiples

Mostram gráficos repetidos por categoria.

Exemplo:
- Vendas por estado  
- Desempenho por produto  

---

## 🔹 Decomposition Tree

Usado para:
- Identificar causas  
- Explorar drivers de métricas  
- Análise explicativa  

---

## 📚 Links Oficiais

- Visualization types:  
  https://learn.microsoft.com/power-bi/visuals/power-bi-visualization-types
