
---

> **As consultas avançadas permitem extrair, transformar e analisar dados de forma mais eficiente e poderosa. Elas combinam múltiplas tabelas, filtros complexos, agregações, funções especiais, subconsultas e técnicas para otimizar performance. Dominar queries avançadas é essencial para resolver problemas reais em sistemas de produção, BI e desenvolvimento fullstack.**

---

# 🔍 **1. Joins Avançados**

### **1.1 INNER JOIN múltiplos**

Retorna linhas que possuem correspondência em todas as tabelas envolvidas.

`SELECT p.nome, c.nome AS categoria, u.nome AS vendedor FROM produtos p INNER JOIN categorias c ON p.categoria_id = c.id INNER JOIN usuarios u ON p.vendedor_id = u.id;`

---

### **1.2 LEFT JOIN com condições**

`SELECT u.nome, p.nome AS produto FROM usuarios u LEFT JOIN produtos p ON u.id = p.vendedor_id AND p.ativo = 1;`

---

### **1.3 SELF JOIN**

Usado quando a tabela se relaciona consigo mesma (hierarquias):

`SELECT f.nome AS funcionario, g.nome AS gerente FROM funcionarios f LEFT JOIN funcionarios g ON f.gerente_id = g.id;`

---

# 🔢 **2. Consultas com Funções Avançadas**

### **2.1 Funções de Data**

`SELECT nome, DATE_FORMAT(data_criacao, '%d/%m/%Y') AS criada_em FROM usuarios;`

### **2.2 Funções Matemáticas**

`SELECT produto, preco, ROUND(preco * 1.1, 2) AS preco_ajustado FROM produtos;`

### **2.3 Funções Condicionais**

`SELECT nome,        IF(ativo = 1, 'Ativo', 'Inativo') AS status FROM usuarios;`

---

# 📊 **3. Agrupamentos Avançados (GROUP BY e HAVING)**

### **3.1 Agrupamento com múltiplas colunas**

`SELECT categoria_id, vendedor_id, COUNT(*) AS total FROM produtos GROUP BY categoria_id, vendedor_id;`

### **3.2 Filtro pós-agrupamento (HAVING)**

`SELECT vendedor_id, COUNT(*) AS total_vendas FROM vendas GROUP BY vendedor_id HAVING total_vendas > 10;`

---

# 🔁 **4. Subconsultas (Subqueries)**

### **4.1 Subquery no WHERE**

`SELECT nome FROM produtos WHERE preco > (SELECT AVG(preco) FROM produtos);`

### **4.2 Subquery no FROM (tabela derivada)**

`SELECT media, MAX(media) FROM (SELECT categoria_id, AVG(preco) AS media       FROM produtos       GROUP BY categoria_id) AS t;`

### **4.3 Subquery correlacionada**

Depende da linha atual do SELECT externo:

`SELECT nome,        (SELECT COUNT(*) FROM vendas v WHERE v.produto_id = p.id) AS total_vendas FROM produtos p;`

---

# 🧮 **5. Window Functions (Funções de Janela)**

_(Muito usadas em análises modernas)_

### **5.1 Ranking**

`SELECT nome, preco,        RANK() OVER(ORDER BY preco DESC) AS ranking_preco FROM produtos;`

### **5.2 Partição por categoria**

`SELECT nome, categoria_id, preco,        AVG(preco) OVER(PARTITION BY categoria_id) AS media_categoria FROM produtos;`

---

# 🔄 **6. UNION e UNION ALL**

### **UNION ALL (mantém duplicatas):**

`SELECT nome FROM clientes_ativos UNION ALL SELECT nome FROM clientes_inativos;`

### **UNION (remove duplicatas):**

`SELECT email FROM newsletter UNION SELECT email FROM usuarios;`

---

# ⚙️ **7. CTEs (Common Table Expressions — WITH)**

Deixa consultas complexas mais legíveis.

`WITH produtos_caros AS (     SELECT * FROM produtos WHERE preco > 100 ) SELECT * FROM produtos_caros WHERE categoria_id = 3;`

---

# 🚀 **8. Otimização de Queries (Performance)**

### **Use índices**

`CREATE INDEX idx_email ON usuarios(email);`

### **Evite LIKE com wildcard no início**

❌ `LIKE "%texto"`  
✔️ `LIKE "texto%"`

### **Evite SELECT ***

Espécie de antipat padrão.

### **Prefira JOIN ao invés de subqueries complexas**

---

# 🧠 **Lembretes Importantes**

- Queries avançadas resolvem problemas que simples SELECT não resolvem.
    
- JOINs são base do trabalho real com MySQL.
    
- HAVING é sempre depois do GROUP BY.
    
- Subqueries podem ser mais lentas — use CTEs quando possível.
    
- Window Functions não substituem GROUP BY — fazem coisas diferentes.
    

---

# 🧪 **Exemplos Práticos para Treinar**

1. Listar top 3 produtos mais vendidos por categoria.
    
2. Encontrar clientes que gastaram acima da média total.
    
3. Criar ranking mensal de vendas por vendedor.
    
4. Montar relatório com agregação + janela (ex.: crescimento mês a mês).
    
5. Criar CTE para dividir consulta enorme em etapas.
    

---

# 🌱 **Dicas de Estudo**

- Comece pelo básico, mas refine com JOINs complexos.
    
- Resolva problemas reais: relatórios, dashboards, filtros avançados.
    
- Repita exercícios alterando filtros, colunas e agrupamentos.
    
- Não decore — **entenda a lógica de combinação de tabelas**.
    
- Use o MySQL Workbench para visualizar e testar consultas pesadas.