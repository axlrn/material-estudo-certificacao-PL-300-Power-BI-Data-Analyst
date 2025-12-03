# ⭐ Boas Práticas de Modelagem

Estas práticas garantem um modelo limpo, eficiente e fácil de manter.

---

## ✔ Usar Modelo Estrela

- Tabelas fato no centro  
- Dimensões ao redor  
- Evitar snowflake (normalização excessiva)  

---

## ✔ Criar Medidas Explícitas

Evitar medidas automáticas (implícitas). Sempre crie medidas no painel **Modeling > New Measure**.

---

## ✔ Nomear Tabelas e Medidas Claramente

Exemplos:

- `Fato Vendas`  
- `Dim Produto`  
- `[Total Vendas]`  
- `[Qtd Clientes Ativos]`  

---

## ✔ Criar Pastas de Exibição (Display Folders)

Organizar medidas:

- _01 KPIs  
- _02 Time Intelligence  
- _03 Métricas Financeiras  

---

## ✔ Evitar Colunas Calculadas (quando possível)

Preferir medidas:

- consumem menos memória  
- não aumentam tamanho do modelo  

---

## ✔ Usar Tabela de Datas Oficial

Com colunas:

- Data  
- Ano  
- Mês  
- Trimestre  
- Semana ISO  

---

## ✔ Documentar o Modelo

Utilizar:

- Descrições  
- Linhas de anotação  
- Notas no GitHub  

---

## 📚 Links Oficiais

- Data Modeling Guidance:  
  https://learn.microsoft.com/power-bi/guidance/  
