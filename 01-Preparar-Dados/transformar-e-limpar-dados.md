# 🔧 Transformar e Limpar Dados com Power Query

Este módulo aborda a etapa de **transformação**, fundamental para garantir qualidade, consistência e estrutura do dataset.

---

## 🔹 Categorias de Transformações

### ✔ Estrutura
- Remover linhas  
- Remover colunas  
- Dividir colunas  
- Transpor dados  
- Agrupar por  

### ✔ Qualidade
- Remover duplicatas  
- Detectar e corrigir erros  
- Substituir valores  
- Preencher valores  

### ✔ Tipos de dados
- Conversão para inteiro, decimal, data, texto  
- Detecção automática x manual  

---

## 🔹 Ferramentas importantes

### **Column Profile**
Exibe estatísticas detalhadas:
- Valores distintos  
- Valores vazios  
- Mínimo/máximo  
- Distribuição  

### **Column Quality**
Mostra:
- Porcentagem válida  
- Erros  
- Valores vazios  

### **Column Distribution**
Histograma por coluna  

---

## 🔹 Mesclar Tabelas (JOIN)
Power Query suporta:

- Left Outer (mais comum)  
- Right Outer  
- Inner  
- Full Outer  
- Anti Joins  

Aplicações típicas:
- Unir tabelas fato e dimensão  
- Acrescentar parâmetros externos  
- Substituir *VLOOKUP* do Excel  

---

## 🔹 Anexar Tabelas (APPEND)
Usado para empilhar tabelas com **mesma estrutura**, como:

- Múltiplos arquivos CSV de meses diferentes  
- Logs diários  
- Exportações de sistemas  

---

## 🔹 Query Folding

Folding é quando o Power Query **empurra transformações para a fonte de dados**.

Transformações que geralmente mantêm folding:

- Filtrar linhas  
- Selecionar colunas  
- Agrupar  
- Join  
- Alterar tipos  

Transformações que quebram folding:

- Colunas personalizadas complexas  
- Passos que exigem processamento local  

---

## 📚 Links Oficiais

- Power Query transformations:  
  https://learn.microsoft.com/power-query/transformation-section  

---
