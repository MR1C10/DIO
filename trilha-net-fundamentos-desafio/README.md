# Sistema de Estacionamento - Desafio DIO

Este projeto é uma resolução do desafio de fundamentos de .NET da DIO, que consiste em criar um sistema de gerenciamento de estacionamento.

## 📋 Sobre o Projeto

O sistema permite gerenciar veículos em um estacionamento, oferecendo funcionalidades para:
- Cadastrar veículos
- Remover veículos e calcular o valor a ser pago
- Listar todos os veículos estacionados

## 🎯 Objetivos do Desafio

O desafio tinha como objetivo praticar conceitos fundamentais de programação em C#, incluindo:
- Orientação a objetos
- Manipulação de listas
- Estruturas de controle (loops, condicionais)
- Interação com o usuário via console
- Cálculos matemáticos

## 🏗️ Estrutura do Projeto

```
DesafioFundamentos/
├── Models/
│   └── Estacionamento.cs     # Classe principal com a lógica do negócio
├── Program.cs                # Ponto de entrada da aplicação
└── DesafioFundamentos.csproj # Arquivo de configuração do projeto
```

## 💡 Solução Implementada

### Classe Estacionamento

A classe `Estacionamento` foi implementada com os seguintes componentes:

#### Propriedades Privadas
- `precoInicial`: Valor fixo cobrado ao estacionar
- `precoPorHora`: Valor cobrado por hora de permanência
- `veiculos`: Lista para armazenar as placas dos veículos

#### Métodos Implementados

**1. Construtor**
```csharp
public Estacionamento(decimal precoInicial, decimal precoPorHora)
```
Inicializa o estacionamento com os preços definidos.

**2. AdicionarVeiculo()**
- Solicita a placa do veículo ao usuário
- Adiciona a placa à lista de veículos
- Confirma o cadastro

**3. RemoverVeiculo()**
- Solicita a placa do veículo a ser removido
- Verifica se o veículo está na lista (comparação case-insensitive)
- Se encontrado:
  - Solicita a quantidade de horas estacionadas
  - Calcula o valor total: `precoInicial + (precoPorHora * horas)`
  - Remove o veículo da lista
  - Exibe o valor total a ser pago
- Se não encontrado: exibe mensagem de erro

**4. ListarVeiculos()**
- Verifica se há veículos cadastrados
- Se houver: exibe lista numerada dos veículos
- Se não houver: informa que não há veículos estacionados

### Program.cs

O arquivo principal implementa:
- Configuração de encoding UTF-8 para acentuação
- Coleta dos preços inicial e por hora
- Menu interativo com 4 opções
- Loop principal para manter o programa executando
- Tratamento básico de opções inválidas

## 🔧 Funcionalidades

### Menu Principal
1. **Cadastrar veículo** - Adiciona um novo veículo ao estacionamento
2. **Remover veículo** - Remove um veículo e calcula o valor a ser pago
3. **Listar veículos** - Mostra todos os veículos atualmente estacionados
4. **Encerrar** - Finaliza o programa

### Características da Implementação

- **Busca case-insensitive**: O sistema não diferencia maiúsculas de minúsculas ao buscar placas
- **Validação de presença**: Verifica se o veículo está realmente estacionado antes de removê-lo
- **Cálculo automático**: Calcula automaticamente o valor total baseado no tempo de permanência
- **Interface amigável**: Menu limpo e mensagens claras para o usuário

## 🚀 Como Executar

1. Certifique-se de ter o .NET 6.0 ou superior instalado
2. Clone o repositório
3. Navegue até a pasta do projeto:
   ```bash
   cd trilha-net-fundamentos-desafio/DesafioFundamentos
   ```
4. Execute o projeto:
   ```bash
   dotnet run
   ```

## 📊 Exemplo de Uso

```
Seja bem vindo ao sistema de estacionamento!
Digite o preço inicial: 2,00
Agora digite o preço por hora: 1,50

Digite a sua opção:
1 - Cadastrar veículo
2 - Remover veículo  
3 - Listar veículos
4 - Encerrar

> 1
Digite a placa do veículo para estacionar: ABC-1234
Veiculo cadastrado!

> 2
Digite a placa do veículo para remover: ABC-1234
Digite a quantidade de horas que o veículo permaneceu estacionado: 3
O veículo ABC-1234 foi removido e o preço total foi de: R$ 6,50
```

## 🛠️ Tecnologias Utilizadas

- **C#**: Linguagem de programação
- **.NET 8.0**: Framework de desenvolvimento
- **Console Application**: Tipo de aplicação

## 📝 Observações

- O projeto demonstra conceitos fundamentais de programação orientada a objetos
- A implementação é simples mas funcional, adequada para fins didáticos
- O código está bem estruturado e seguindo boas práticas básicas de C#

---

**Desenvolvido como parte do bootcamp de .NET da DIO** 🎓
