# Sistema de Reserva de Salas

## Equipe
- Antonio Helder Batista Lima Marreiro
- João Guilherme Lins Almeida 

## Descrição do Projeto
Este projeto tem como objetivo desenvolver um sistema para *reserva de salas*, permitindo que usuários agendem espaços disponíveis.

# Diagramas do Sistema

## Diagrama de Classes UML

      +---------------+      +----------------+      +--------------+
      |    Usuário    |      |   Reserva     |       |    Sala      |
      +---------------+      +---------------+       +--------------+
      |  - nome       | 1 ───| - idReserva   |──── 1 | - idSala     |
      |  - email      |      | - data        |       | - número     |
      |  - telefone   |      | - horário     |       | - capacidade |
      +---------------+      +---------------+       +--------------+

## Explicação do Modelo:
- Usuário e Reserva: Um usuário pode fazer várias reservas, mas cada reserva é realizada por um único usuário.
- Reserva e Sala: Cada reserva está associada a uma sala específica, mas uma sala pode ter várias reservas.

## Fluxo BPMN

[INÍCIO] ---> [Usuário acessa o sistema] ---> [Seleciona sala e horário] ---> [Verifica disponibilidade] ---> <br>
{Sala disponível?} <br>
   ├──► [SIM] →    [Reserva confirmada] → [FIM] <br>
   └──► [NÃO] →   [Exibe salas alternativas] → [FIM] <br>
