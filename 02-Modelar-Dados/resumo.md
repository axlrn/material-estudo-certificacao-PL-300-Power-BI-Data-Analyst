# 🧩 Resumo – Modelar Dados

Este módulo aborda os princípios essenciais de **modelagem dimensional**, relações entre tabelas, DAX, desempenho e estruturação de modelos eficientes no Power BI.

---

## 🎯 Objetivos do módulo

- Construir modelos eficientes baseados em **tabelas fato e dimensões**  
- Configurar relacionamentos e cardinalidades  
- Criar medidas com DAX  
- Implementar hierarquias  
- Controlar direcionalidade de filtros  
- Otimizar desempenho do modelo  

---

## 🔹 Tópicos Principais

### 1. Modelo Estrela (Star Schema)
Estrutura padrão recomendada pela Microsoft:

- Tabelas fato → métricas, granularidade definida  
- Tabelas dimensão → atributos descritivos  
- Minimiza duplicidades, melhora performance e compressão

---

### 2. Relacionamentos
Propriedades:

- Cardinalidade: 1:*, *:1, *:*  
- Direcionalidade: single vs. both  
- Cross-filtering  
- Relacionamentos ativos e inativos (USERELATIONSHIP)  

---

### 3. DAX – medidas e cálculos
Tipos comuns:

- Medidas implícitas vs. explícitas  
- Funções de agregação  
- Time intelligence  
- Contextos: linha, filtro e avaliação  

---

### 4. Otimização de Modelos
Inclui:

- Remoção de colunas irrelevantes  
- Minimização de cardinalidade  
- Redução de relacionamentos desnecessários  
- Gerenciamento de tabelas intermediárias  
- Uso correto de data table  

---

## 📚 Links Oficiais

- Data modeling best practices  
  https://learn.microsoft.com/power-bi/guidance/star-schema  
- Relationships in Power BI  
  https://learn.microsoft.com/power-bi/transform-model/desktop-relationships  

---

## ✅ Checklist de Estudos

- [ ] Criar um modelo estrela com fato e dimensões  
- [ ] Configurar relacionamentos corretamente  
- [ ] Criar medidas básicas e avançadas em DAX  
- [ ] Utilizar funções de time intelligence  
- [ ] Reduzir cardinalidade de colunas pesadas  
