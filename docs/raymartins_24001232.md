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

# 6. Documentação dos Casos de Uso:

---

## UC01 — Realizar Venda
### Ator Principal: 
Atendente
  
### Descrição: 
Permite registrar a venda de um ou mais produtos para um cliente.  

### Pré-condições:  
- Atendente autenticado no sistema
- Produto cadastrado no sistema

### Pós-condições:  
- Venda registrada
- Estoque atualizado
- Comprovante gerado

### Fluxo Principal
1) Atendente inicia o processo de venda.
2) Sistema solicita identificação do cliente.
3) Atendente informa o cliente.
4) Sistema informa quantidade do produto solicitado.
5) Atendente informa a quantidade desejada.
6) Sistema calcula o valor total da venda.
7) Atendente confirma a venda.
8) Sistema registra venda e atualiza o estoque.
9) Sistema emite o comprovante da venda.

### Fluxos Alternativos / Exceções
- **FA01 — Cliente não cadastrado**
O sistema permite realizar o cadastro rápido do cliente.

- **FA02 — Estoque insuficiente**
O sistema informa que não há quantidade suficiente e impede a venda.


### Relacionamentos
**Include:** 
- Consultar Produto
- Verificar Estoque
- Emitir Comprovante

**Extend:** 
- Cadastrar Cliente
- Registrar Venda a Prazo



## UC02 — Consultar Produto
### Ator Principal: 
Atendente
  
### Descrição: 
Permite pesquisar produtos disponíveis no sistema.  

### Pré-condições:  
- Produto cadastrado no sistema

### Pós-condições:  
- Produto exibido na tela

### Fluxo Principal
1) Atendente acessa a função de consulta.
2) Atendente informa nome, código de barras ou fabricante.
3) Sistema busca o produto no banco de dados.
4) Sistema apresenta as informações do produto.

### Fluxos Alternativos / Exceções
- **FA01 — Produto não encontrado**
O sistema informa que o produto não está cadastrado.

### Relacionamentos
**Include:** 
—

**Extend:** 
—



## UC03 — Verificar Estoque
### Ator Principal: 
Sistema
  
### Descrição: 
Verificar se há quantidade suficiente no estoque. 

### Pré-condições:  
- Produto selecionado

### Pós-condições:  
- Quantidade disponível exibida

### Fluxo Principal
1) Sistema recebe produto selecionado.
2) Sistema consulta o estoque da unidade.
3) Sistema retorna a quantidade disponível.

### Fluxos Alternativos / Exceções
- **FA01 — Produto sem estoque**
O sistema informa indisponibilidade do produto.

### Relacionamentos
**Include:** 
—

**Extend:** 
—



## UC04 — Emitir Comprovante
### Ator Principal: 
Sistema
  
### Descrição: 
Gera o comprovante da venda realizada.

### Pré-condições:  
- Venda registrada no sistema

### Pós-condições:  
- Comprovante exibido ou impresso

### Fluxo Principal
1) Sistema recebe os dados da venda.
2) Sistema gera o comprovante.
3) Sistema exibe ou imprime o comprovante.

### Fluxos Alternativos / Exceções
- **FA01 — Falha na impressão**
O sistema permite reemitir o comprovante.

### Relacionamentos
**Include:** 
—

**Extend:** 
—



## UC05 — Cadastrar Cliente
### Ator Principal: 
Atendente
  
### Descrição: 
Permite registrar um novo cliente no sistema.

### Pré-condições:  
- Cliente não cadastrado

### Pós-condições:  
- Cliente registrado no sistema

### Fluxo Principal
1) Atendente seleciona cadastrar cliente.
2) Atendente informa os dados do cliente.
3) Sistema valida os dados.
4) Sistema salva o cadastro.

### Fluxos Alternativos / Exceções
- **FA01 — Dados inválidos**
O sistema solicita correção das informações.

### Relacionamentos
**Include:** 
—

**Extend:** 
- Realizar Venda



## UC06 — Registrar Venda a Prazo
### Ator Principal: 
Atendente
  
### Descrição: 
Permite registrar uma venda que será paga posteriormente.

### Pré-condições:  
- Cliente identificado

### Pós-condições:  
- Conta a receber gerada

### Fluxo Principal
1) Atendente seleciona pagamento a prazo.
2) Sistema solicita data de vencimento.
3) Atendente informa a data.
4) Sistema registra a conta a receber.

### Fluxos Alternativos / Exceções
- **FA01 — Cliente sem cadastro válido**
O sistema solicita cadastro do cliente.

### Relacionamentos
**Include:** 
- Registrar Conta a Receber

**Extend:** 
- Realizar Venda



## UC07 — Registrar Conta a Receber
### Ator Principal: 
Sistema/Financeiro
  
### Descrição: 
Registra valores a receber originados de vendas a prazo.

### Pré-condições:  
- Venda a prazo registrada

### Pós-condições:  
- Conta registrada no sistema

### Fluxo Principal
1) Sistema recebe dados da venda a prazo.
2) Sistema registra descrição e valor.
3) Sistema registra data de vencimento.
4) Sistema define status como "Aberta".

### Fluxos Alternativos / Exceções
- **FA01 — Dados incompletos**
O sistema solicita correção das informações.

### Relacionamentos
**Include:** 
—

**Extend:** 
—



## UC08 — Cadastrar Produto
### Ator Principal: 
Gerente
  
### Descrição: 
Permite registrar novos produtos no sistema.

### Pré-condições:  
- Usuário autenticado como gerente

### Pós-condições:  
- Produto cadastrado no sistema

### Fluxo Principal
1) Gerente acessa cadastro de produtos.
2) Gerente informa descrição, preço e fabricante.
3) Sistema valida os dados.
4) Sistema salva o produto.

### Fluxos Alternativos / Exceções
- **FA01 — Produto já existente**
O sistema informa que o produto já está cadastrado.

### Relacionamentos
**Include:** 
—

**Extend:** 
—



## UC09 — Atualizar Estoque
### Ator Principal: 
Sistema
  
### Descrição: 
Atualiza automaticamente o estoque após uma venda.

### Pré-condições:  
- Venda registrada

### Pós-condições:  
- Quantidade do produto atualizada

### Fluxo Principal
1) Sistema recebe os dados da venda.
2) Sistema calcula nova quantidade de estoque.
3) Sistema atualiza o estoque da unidade.

### Fluxos Alternativos / Exceções
- **FA01 — Erro de atualização**
O sistema registra erro e notifica o administrador.

### Relacionamentos
**Include:** 
— 

**Extend:** 
—



## UC10 — Gerar Relatórios
### Ator Principal: 
Gerente / Financeiro
  
### Descrição: 
Permite gerar relatórios gerenciais do sistema.

### Pré-condições:  
- Usuário autenticado

### Pós-condições:  
- Relatório exibido ou exportado

### Fluxo Principal
1) Usuário seleciona o tipo de relatório.
2) Sistema coleta os dados necessários.
3) Sistema gera o relatório.
4) Sistema apresenta o resultado.

### Fluxos Alternativos / Exceções
- **FA01 — Dados indisponíveis**
O sistema informa que não há dados para o relatório.

### Relacionamentos
**Include:** 
— 

**Extend:** 
—
