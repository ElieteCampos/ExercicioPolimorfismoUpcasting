# 💼 Sistema de Pagamento de Funcionários

Este projeto em C# tem como objetivo calcular o pagamento de funcionários, considerando dois tipos: **comuns** e **terceirizados**. O sistema demonstra conceitos fundamentais de **programação orientada a objetos**, como **herança** e **polimorfismo**.

## 🧾 Descrição do Funcionamento

O programa solicita ao usuário o número total de funcionários e, para cada um, pergunta:

- Se o funcionário é terceirizado (`y/n`)
- Nome
- Horas trabalhadas
- Valor por hora
- (Se terceirizado) Valor adicional

Com base nas respostas, o sistema cria um objeto `Employee` ou `OutsourcedEmployee` e o adiciona a uma lista. Por fim, exibe os pagamentos de todos os funcionários.

## 🧱 Estrutura do Projeto

### Classes utilizadas:

- **Employee**
  - Propriedades:
    - `Name`
    - `Hours`
    - `ValuePerHour`
  - Método:
    - `Payment()`: calcula o pagamento normal (horas * valor por hora)

- **OutsourcedEmployee** (herda de `Employee`)
  - Propriedade adicional:
    - `AdditionalCharge`
  - Método sobrescrito:
    - `Payment()`: calcula o pagamento com acréscimo de 110% do valor adicional

### Lógica principal (`Main`):

- Lê os dados do usuário
- Cria os objetos correspondentes
- Armazena os objetos em uma lista de `Employee`
- Exibe os pagamentos utilizando polimorfismo

## 🧠 Conceitos Aplicados

- **Herança:** a classe `OutsourcedEmployee` herda de `Employee`
- **Polimorfismo:** a chamada `emp.Payment()` executa o método adequado conforme o tipo do objeto
- **Coleções genéricas:** uso de `List<Employee>`
- **Cultura Invariant:** garante o uso correto de ponto como separador decimal (`CultureInfo.InvariantCulture`)

## 💻 Exemplo de Execução

- Enter the number of employees: 2
- Employee #1 data:
- Outsourced (y/n)? n
- Name: Maria
- Hours: 40
- Value per hour: 25.00

- Employee #2 data:
- Outsourced (y/n)? y
- Name: João
- Hours: 60
- Value per hour: 30.00
- Additional charge: 200.00

- PAYMENTS:
- Maria - $ 1000.00
- João - $ 2300.00


