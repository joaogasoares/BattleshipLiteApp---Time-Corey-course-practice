# 🚢 Battleship Lite App

Este é uma aplicação de console que simula o clássico jogo de tabuleiro "Batalha Naval". Este projeto foi desenvolvido como o projeto de conclusão (Capstone Project) da seção de Fundamentos de C# do curso **C# Masterclass** do **Tim Corey**.

O objetivo principal deste projeto não é apenas criar um jogo, mas demonstrar o domínio de **Lógica de Programação**, **Programação Orientada a Objetos (POO)** e, crucialmente, a **Separação de Responsabilidades (Separation of Concerns)**.

## 📋 Sobre o Projeto

O jogo permite que dois jogadores (ou um jogador vs lógica simples) posicionem seus navios em um grid e tentem afundar a frota do oponente através de coordenadas (ex: A5, B2).


### Funcionalidades
* **Grid Dinâmico:** Criação e gerenciamento de um tabuleiro de jogo (geralmente 5x5 para a versão Lite).
* **Posicionamento de Navios:** Validação lógica para garantir que os navios não se sobreponham e estejam dentro dos limites.
* **Sistema de Turnos:** Alternância entre jogadores para realizar os disparos.
* **Rastreamento de Tiros:** O sistema registra e informa se o tiro foi um acerto ("Hit") ou erro ("Miss").
* **Condição de Vitória:** Detecção automática quando todos os navios de um oponente foram afundados.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** C#
* **Framework:** .NET (Core / 5 / 6 / 8 - *ajuste conforme sua versão*)
* **Tipo de Aplicação:** Console Application

## 🏗️ Arquitetura e Design

Seguindo os ensinamentos do curso, a solução é dividida para respeitar o princípio de **Single Responsibility Principle (SRP)**:

### 1. BattleshipLibrary (Class Library)
Contém toda a lógica de negócios e os modelos de dados. Esta biblioteca **não** possui código de interface de usuário (sem `Console.WriteLine` ou `Console.ReadLine`).
* **Modelos:** `GridModel`, `PlayerModel`, `ShipModel` (ou nomes similares usados no seu código).
* **Lógica:** Verificação de posições, registro de tiros, verificação de status do jogo.

### 2. BattleshipLite (Console UI)
Responsável apenas pela interação com o usuário.
* Coleta inputs do usuário.
* Exibe as mensagens e o grid no console.
* Chama os métodos da `BattleshipLibrary`.


## Como Executar

Para rodar o projeto localmente, siga os passos abaixo:

### Pré-requisitos
* [SDK do .NET](https://dotnet.microsoft.com/download) instalado.
* Um editor de código (VS Code, Visual Studio, ou Rider).

### Instalação

1. Clone o repositório:
   ```bash
   git clone [https://github.com/SEU-USUARIO/battleship-lite.git](https://github.com/SEU-USUARIO/battleship-lite.git)
