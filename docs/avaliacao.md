# Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante**

Aluno: Ray Martins Ajudarte Eleoterio  
RA: 24001232  
Data: 26/03/2026  

---

# 1. Definição do MVP
O MVP deste sistema foi definido com foco no processo de venda em uma unidade da farmácia, permitindo registrar vendas de produtos, identificar clientes e manter o controle básico de estoque.

Dentro do MVP estão incluídas as seguintes funcionalidades:

- consulta de produtos por nome, código de barras ou fabricante.
- cadastro rápido de clientes.
- registro de vendas de produtos.
- verificação automática de disponibilidade em estoque.
- atualização automática do estoque após a venda.
- emissão de comprovante de venda.
- registro de vendas a prazo com geração automática de contas a receber.

Essas funcionalidades foram escolhidas porque representam o fluxo principal de operação de uma farmácia, ou seja, o atendimento ao cliente no balcão e o registro das vendas realizadas.

Ficam fora do MVP, sendo previstos para versões futuras do sistema:

- gerenciamento completo de compras com fornecedores.
- gestão detalhada de contas a pagar.
- geração avançada de relatórios gerenciais.
- transferências de estoque entre unidades.
- administração completa de usuários e permissões.

Essas funcionalidades não foram incluídas inicialmente porque, embora importantes para a gestão da rede de farmácias, não são essenciais para que o sistema comece a operar e registrar vendas, que é o processo mais crítico para o funcionamento da farmácia.

O MVP permite que o sistema de gestão comece a ser utilizado rapidamente nas unidades da farmácia, focando inicialmente no processo mais crítico do negócio e permitindo futuras expansões para outros módulos do sistema.

---

# 2. Regras de Negócio:

**RN01 — Controle de estoque automático**  
Toda venda, devolução, transferência, perda ou compra deve atualizar automaticamente o estoque da unidade.

**RN02 — Venda condicionada ao estoque disponível**  
Produtos só podem ser vendidos caso exista quantidade suficiente no estoque da unidade.

**RN03 — Venda de medicamentos controlados**  
Medicamentos que exigem receita médica devem ser validados por um farmacêutico antes da conclusão da venda.

**RN04 — Geração automática de contas a receber**  
Vendas realizadas a prazo devem gerar automaticamente um registro em contas a receber com data de vencimento.

**RN05 — Geração automática de contas a pagar**  
Toda compra realizada com fornecedores deve gerar automaticamente um registro em contas a pagar.

**RN06 — Controle de estoque mínimo**
O sistema deve alertar gerentes quando a quantidade de um produto estiver abaixo do nível mínimo configurado.

**RN07 — Restrição por perfil de usuário**
Cada tipo de usuário poderá acessar apenas as funcionalidades permitidas ao seu perfil.

---

# 3. Requisitos Funcionais:

**RF01 — Cadastrar clientes**  
O sistema deve permitir o cadastro de novos clientes.

**RF02 — Consultar produtos**  
O sistema deve permitir buscar produtos por nome, código de barras ou fabricante.

**RF03 — Registrar vendas**  
O sistema deve permitir registrar vendas de produtos para clientes.

**RF04 — Registrar vendas a prazo**  
O sistema deve permitir registrar vendas a prazo vinculadas ao cliente.

**RF05 — Emitir comprovante de venda**  
O sistema deve gerar um comprovante ao final da venda.

**RF06 — Cadastrar e atualizar produtos**  
Gerentes devem poder cadastrar novos produtos e atualizar suas informações.

**RF07 — Registrar compras de fornecedores**  
O sistema deve registrar compras feitas junto aos fornecedores.

**RF08 — Gerenciar contas a pagar**  
O sistema deve permitir registrar e acompanhar contas a pagar.

**RF09 — Gerenciar contas a receber**  
O sistema deve permitir registrar e acompanhar contas a receber.

**RF10 — Gerar relatórios gerenciais**  
O sistema deve permitir a geração de relatórios de vendas, estoque e financeiro.

---

# 4. Requisitos Não Funcionais:

**RNF01 — Segurança e controle de acesso**  
O sistema deve possuir autenticação de usuários com controle de permissões baseado em perfil.

**RNF02 — Desempenho**  
Consultas de produtos e registro de vendas devem ocorrer em tempo inferior a 2 segundos.

**RNF03 — Disponibilidade**  
O sistema deve estar disponível para uso durante todo o horário de funcionamento das unidades.

**RNF04 — Integridade dos dados**  
Todas as transações de venda, compra e estoque devem garantir consistência dos dados.

**RNF05 — Usabilidade**  
A interface deve ser simples e intuitiva para facilitar o uso pelos atendentes.

---

# 5. Casos de Uso:
### Inserir **diagrama de casos de uso geral**, demonstrando claramente:
- os 10 casos
- relação entre eles e atores
- pelo menos 3 includes
- pelo menos 3 extends

---

# 6. Documentação dos Casos de Uso
Para **cada caso de uso**, utilize o template abaixo:
---

## **UCXX — Nome do Caso de Uso**
**Ator(es):**  
**Descrição:**  
**Pré-condições:**  
**Pós-condições:**  

### Fluxo Principal
1.  
2.  
3.  
4.  

### Fluxos Alternativos / Exceções
- FA01 —  
- FA02 —  

### Relacionamentos
- **Include:** (listar quando aplicável)  
- **Extend:** (listar quando aplicável)  

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

---

> Repita essa estrutura para **todos os seus casos de uso** (mínimo 10).


