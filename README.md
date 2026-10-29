# Banco digital em Java — estudo de orientação a objetos

Simulação de operações bancárias no console para praticar abstração, encapsulamento, herança e polimorfismo. O projeto representa clientes, contas correntes e contas poupança com classes e interfaces Java.

## Funcionalidades implementadas

- Criar contas correntes e poupanças associadas a um cliente.
- Atribuir agência padrão e números sequenciais às contas.
- Depositar, sacar e transferir valores entre contas.
- Imprimir os dados do titular, da conta e do saldo.

## Organização do código

| Arquivo | Responsabilidade |
| --- | --- |
| `Cliente.java` | Dados do titular |
| `IConta.java` | Contrato das operações bancárias |
| `Conta.java` | Classe abstrata com saldo e operações comuns |
| `ContaCorrente.java`, `ContaPoupanca.java` | Tipos de conta e impressão de extrato |
| `Banco.java` | Modelo de banco com nome e lista de contas |
| `Main.java` | Demonstração das operações |

## Como executar

Requer um JDK com `javac` e `java` disponíveis. Na raiz do repositório:

```sh
git clone https://github.com/JoaoAlencar00/Desafio-BancoDigital.git
cd Desafio-BancoDigital
mkdir build
javac -encoding UTF-8 -d build *.java
java -cp build Main
```

O exemplo cria duas contas para o cliente Venilton, deposita 100 na conta corrente e transfere esse valor para a poupança. Ao final, imprime os saldos 0,00 e 100,00, respectivamente.

## Conceitos praticados

- **Abstração:** representação das entidades e operações do domínio bancário.
- **Encapsulamento:** acesso ao estado por meio dos métodos das classes.
- **Herança:** reutilização de comportamento a partir de `Conta`.
- **Polimorfismo:** operações definidas pelo contrato `IConta` e pela classe abstrata.

## Escopo atual

O programa executa uma demonstração fixa no console. Os dados ficam em memória e não há API HTTP, autenticação, banco de dados ou menu interativo.

As operações ainda não validam saldo disponível, valores negativos ou conta de destino nula. O saldo usa `double`; a implementação serve ao estudo de POO e não atende às regras de uma aplicação financeira real. Não há testes automatizados no repositório.

## Origem e créditos

Estudo baseado no laboratório [Criando um Banco Digital com Java e Orientação a Objetos](https://github.com/falvojr/lab-banco-digital-oo), de falvojr. Este repositório mantém o exemplo para prática dos conceitos de POO.

[Assistir à mentoria do laboratório](https://www.youtube.com/watch?v=YS6ouOhkyNI).
