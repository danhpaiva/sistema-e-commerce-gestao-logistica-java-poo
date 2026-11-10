# Exercício Prático:<br> Sistema de E-Commerce e Gestão Logística (POO em Java)

**Disciplina:** Algoritmos e Programação

**Professor / Desenvolvedor:** Prof. Daniel Paiva

**Objetivo:** Praticar conceitos de Programação Orientada a Objetos (POO) em Java —<br> como herança múltipla de tipos (via interfaces), polimorfismo, encapsulamento, tratamento de coleções e modelagem de domínios complexos — através do desenvolvimento de uma plataforma robusta de comércio eletrônico.

## 🛒 Contextualização do Problema

Você foi contratado como Desenvolvedor Sênior para estruturar o núcleo de um **Sistema de E-Commerce e Gestão Logística** de grande porte. <br>A aplicação deve ser capaz de gerenciar desde o catálogo de produtos e perfis de clientes até o processamento de carrinhos de compras, fechamento de pedidos, pagamentos, emissão de notas fiscais e rastreamento de entregas logísticas.

Para atender a essa demanda corporativa, o seu projeto deverá ser arquitetado utilizando **no mínimo 14 (quatorze) classes**, integradas e orquestradas a partir da classe principal `Programa.java`.

## 🛠️ Requisitos de Implementação

Para garantir uma arquitetura escalável e bem modularizada, sua aplicação deve contemplar as seguintes classes e estruturas:

### 1. Núcleo de Usuários e Perfis (Mínimo de 3 classes)

1. **`Usuario`** (Classe Abstrata Base): Contém dados genéricos como identificador, nome, e-mail e senha.

2. **`Cliente`** (Herda de `Usuario`): Atributos específicos como CPF, histórico de pedidos e endereço de entrega.

3. **`Administrador`** (Herda de `Usuario`): Atributos e permissões especiais para gerenciamento de catálogo e estoque.

### 2. Módulo de Catálogo e Produtos (Mínimo de 4 classes)

4. **`Produto`** (Classe Abstrata Base): Atributos essenciais como código, nome, preço unitário e estoque disponível.

5. **`ProdutoFisico`** (Herda de `Produto`): Atributos específicos como peso, dimensões e cálculo de frete.

6. **`ProdutoDigital`** (Herda de `Produto`): Atributos específicos como tamanho do arquivo (MB) e link de download.

7. **`Categoria`**: Organiza os produtos por setores (ex: Eletrônicos, Vestuário, Livros).

### 3. Módulo de Vendas e Transações (Mínimo de 4 classes)

8. **`ItemCarrinho`** ou **`ItemPedido`**: Associa um produto à quantidade desejada e calcula o subtotal.

9. **`CarrinhoDeCompras`**: Gerencia a lista de itens adicionados pelo cliente antes do fechamento do pedido.

10. **`Pedido`**: Registra a transação efetivada (contém cliente, lista de itens, status do pedido, valor total e data).

11. **`Pagamento`**: Gerencia a transação financeira (forma de pagamento como Cartão, PIX ou Boleto, status de aprovação e valor).

### 4. Módulo de Logística, Notas e Gestão (Mínimo de 3 classes)

12. **`NotaFiscal`**: Documento fiscal gerado a partir do pedido, contendo impostos calculados e chave de acesso.

13. **`Entrega`** ou **`Rastreio`**: Controla o envio do pedido (código de rastreio, transportadora e status de entrega).

14. **`ECommerce`** (Classe Gerenciadora/Sistema): Classe central que armazena as coleções globais (`List<Cliente>`, `List<Produto>`, `List<Pedido>`, etc.) e centraliza as regras de negócio do sistema.

### 🚀 A Classe Principal (`Programa.java`)

A classe `Programa.java` deve conter o método `public static void main(String[] args)` e simular o fluxo completo de uma loja virtual:

1. Instanciar a classe gerenciadora (`ECommerce`).

2. Cadastrar administradores e clientes na plataforma.

3. Cadastrar diferentes tipos de produtos (`ProdutoFisico` e `ProdutoDigital`) vinculados a categorias.

4. Simular um cliente adicionando produtos ao **`CarrinhoDeCompras`**.

5. Efetivar a compra gerando um **`Pedido`**.

6. Processar o **`Pagamento`** correspondente.

7. Emitir a **`NotaFiscal`** e inicializar a **`Entrega`** logística.

8. Imprimir no console o extrato completo das operações e o estado do sistema.

## 📋 Critérios de Avaliação

* **Organização e Modularidade:** Divisão clara das 14 classes respeitando o princípio de responsabilidade única.

* **Herança e Polimorfismo:** Aproveitamento correto de classes abstratas e sobrecarga/sobrescrita de métodos.

* **Encapsulamento e Segurança:** Atributos privados com getters e setters devidamente validados.

* **Gestão de Coleções:** Uso correto de estruturas de dados (`ArrayList`) na classe gerenciadora.

* **Execução Consistente:** Simulação limpa e sem falhas na classe `Programa.java`.

Bons códigos e boas vendas! 💻📦
