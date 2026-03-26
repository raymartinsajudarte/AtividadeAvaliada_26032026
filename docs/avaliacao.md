# Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante**

Aluno: Ray Martins Ajudarte Eleoterio  
RA: 24001232  
Data: 26/03/2026  

---

# 1. Definição do MVP
Descreva aqui **qual parte do sistema** foi incluída no seu MVP.  
Explique claramente:

- O que está **dentro** do MVP  
- O que está **fora** do MVP  
- Por que você fez essas escolhas  

Exemplo de início:  
> “Meu MVP cobre o processo de venda desde a identificação/cadastro do cliente até a emissão do comprovante, incluindo tratamento de estoque insuficiente.”

---

# 2. Regras de Negócio

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

# 3. Requisitos Funcionais

**RF01 —**  
**RF02 —**  
**RF03 —**  
**RF04 —**  
**RF05 —**  
**RF06 —**  
**RF07 —**  
**RF08 —**  


---

# 🛡 4. Requisitos Não Funcionais (mínimo: 4)
Liste os RNFs do sistema conforme seu MVP.

**RNF01 —**  
**RNF02 —**  
**RNF03 —**  
**RNF04 —**  

(Adicione mais se quiser.)

---

# 5. Casos de Uso (mínimo: 10)
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


