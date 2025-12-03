# 🔐 Segurança em Nível de Linha (RLS)

Row-Level Security (RLS) permite que diferentes usuários vejam apenas os dados autorizados, com base em filtros definidos diretamente no modelo semântico do Power BI.

---

## 🔹 Tipos de RLS

### ✔ Estática
Os filtros são fixos dentro da função criada no modelo.

Exemplo:
```DAX
DimRegiao[Estado] = "SP"
```

### ✔ Dinâmica
Os filtros dependem do usuário conectado, usando funções como `USERPRINCIPALNAME()`.

Exemplo:
```DAX
DimVendedor[Email] = USERPRINCIPALNAME()
```

---

## 🔹 Como Criar Funções de Segurança

1. No Power BI Desktop, vá em **Modeling → Manage Roles**  
2. Clique em **Create**  
3. Defina o nome da função (ex.: "Vendedores_SP")  
4. Aplique o filtro DAX na tabela correspondente  

Exemplo de regra:
```DAX
FatoVendas[Estado] = "SP"
```

---

## 🔹 RLS Dinâmico – Exemplo Completo

Imagine uma dimensão de vendedores:

| Vendedor | Email | Região |
|----------|--------|--------|
| João | joao@empresa.com | Sul |
| Maria | maria@empresa.com | Norte |

Regra dinâmica:
```DAX
DimVendedor[Email] = USERPRINCIPALNAME()
```

O Power BI fará automaticamente o filtro para o usuário conectado no serviço.

---

## 🔹 Testar RLS no Power BI Desktop

1. Vá em **Modeling → View As**  
2. Escolha a função a ser testada  
3. Verifique se o relatório mostra os dados esperados  

Isso evita erros antes da publicação.

---

## 🔹 Configuração no Power BI Service

Após publicar o dataset:

1. Acesse o workspace  
2. Vá em **Datasets → Security**  
3. Escolha a função criada  
4. Adicione usuários ou grupos correspondentes  

Lembre-se:

- **RLS não funciona no “Meu Workspace”**  
- Para apps corporativos, recomenda-se workspaces dedicados e governança ativa  

---

## 🔹 Recomendações Importantes

- Armazene usuários em uma tabela de dimensão quando usar RLS dinâmico  
- Evite relacionamentos bidirecionais  
- Certifique-se de que a coluna usada no filtro está corretamente relacionada às tabelas fato  
- Teste sempre antes de publicar  
- Combine RLS com governança e sensibilidade de dados  

---

## 📚 Links Oficiais

- Documentação RLS:  
  https://learn.microsoft.com/power-bi/enterprise/service-admin-row-level-security  
