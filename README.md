# 🔄 Explorando Workflows Automatizados com AWS Step Functions

 Repositório criado para a entrega do desafio prático do curso **Explorando Workflows Automatizados com AWS Step Functions** pela [DIO (Digital Innovation One)](https://www.dio.me/).

---

## 📌 Descrição do Projeto

Este projeto consiste na criação e documentação de uma **State Machine (Máquina de Estados)** no **AWS Step Functions** utilizando a linguagem **ASL (Amazon States Language)** em padrão **JSONPath**.

O workflow simula o **Processamento de Pedidos em um E-commerce**, orquestrando tomadas de decisão condicionais para validação de estoque e processamento de pagamento com tratamento de falhas contido.

---

## 🛠️ Arquitetura e Fluxo de Trabalho

```[ Início ]
                  │
          [ ValidarPedido ]
                  │
        [ VerificarEstoque ] ──(Fora de Estoque)──► [ NotificarFalhaEstoque ] (Fail)
                  │ (Em Estoque)
         [ ProcessarPagamento ]
                  │
          [ PedidoConcluido ] (Succeed)
                  │
               [ Fim ]
