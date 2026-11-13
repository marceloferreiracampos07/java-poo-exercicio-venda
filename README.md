# 🛒 Sistema de Controle de Vendas e Estoque (Java POO)

Este repositório contém um exercício prático desenvolvido durante meus estudos de **Programação Orientada a Objetos (POO) em Java** (acompanhando a trilha do DevDojo). O objetivo do projeto é simular o cadastro de produtos e a operação de vendas aplicando regras de negócio reais.

## 🚀 Funcionalidades e Regras de Negócio

* **Cadastro Seguro de Produtos:** Inicialização de objetos com `nome`, `preço` e `estoque` através de construtores.
* **Validação de Preço Negativo:** O sistema impede o cadastro ou alteração de produtos com valores menores que zero, lançando uma exceção (`IllegalArgumentException`).
* **Controle de Vendas e Estoque:** O método de venda verifica automaticamente se há saldo suficiente em estoque antes de concluir a operação, calculando o valor total da compra e atualizando a quantidade restante.

## 🧠 Conceitos Aplicados

* **Encapsulamento:** Uso de modificadores de acesso (`private`) para proteger os atributos da classe e métodos *getters* e *setters* para acesso controlado.
* **Referência `this`:** Utilizada no construtor e nos métodos para diferenciar atributos da instância dos parâmetros recebidos.
* **Tratamento de Exceções:** Uso do `IllegalArgumentException` para garantir a integridade dos dados e barrar estados inválidos no objeto.
* **Estruturas Condicionais:** Controle de fluxo para validação de regras de negócio.

## 💻 Exemplo de Uso

```java
// Criando um produto válido e realizando uma venda
Produtoex produto1 = new Produtoex("jogo-gta6", 450.0, 50);
produto1.Vender(40); 
// Saída: 
// o valor total da venda foi : 18000.0
// no estoque resta 10 Unidades do jogo

// Tentando realizar uma venda acima do estoque disponível
Produtoex produto2 = new Produtoex("banana", 60.0, 30);
produto2.Vender(40); 
// Saída: 
// estoque insuficiente
