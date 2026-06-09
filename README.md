# Projeto de Arquitetura e Organização de Computadores I - Processador RISC 4 BITS

## Sobre o Projeto

Este projeto teve como objetivo compreender o funcionamento interno de um processador através da implementação de uma arquitetura simplificada baseada nos conceitos clássicos de computadores.

Durante o desenvolvimento são estudados temas como:

* Arquitetura Von Neumann e Harvard
* Organização da CPU
* Unidade de Controle (UC)
* Unidade Lógica e Aritmética (ULA)
* Registradores
* Hierarquia de Memórias
* Ciclo de Execução de Instruções
* Modos de Endereçamento
* Linguagem Assembly
* Sistema de Interrupções

---

## Componentes da CPU

### Program Counter (PC)

Responsável por armazenar o endereço da próxima instrução que será executada.

#### Funções

* Controlar o fluxo do programa;
* Incrementar automaticamente após cada instrução;
* Alterar o fluxo através de instruções de salto.

---

### Instruction Register (IR)

Armazena temporariamente a instrução buscada na memória ROM.

#### Responsabilidades

* Receber a instrução atual;
* Mantê-la estável durante a decodificação;
* Disponibilizá-la para a Unidade de Controle.

---

### Acumulador (AC)

Registrador utilizado nas operações da Unidade Lógica e Aritmética (ULA).

#### Exemplo

```assembly
MOVL 5
ADDL 3

; Resultado
AC = 8
```

---

### Unidade de Controle (UC)

Coordena todo o funcionamento do processador.

Executa continuamente o ciclo de instruções:

```text
Busca
   ↓
Decodificação
   ↓
Execução
```

Também gera todos os sinais necessários para:

* Leitura da ROM;
* Acesso à RAM;
* Atualização do Program Counter (PC);
* Escrita no Acumulador (AC);
* Controle da Unidade Lógica e Aritmética (ULA).

---

### Unidade Lógica e Aritmética (ULA)

Responsável por executar operações matemáticas e lógicas.

#### Operações suportadas

* Soma
* Subtração
* OR
* NOT
* Shift Left
* Shift Right

Além das operações, a ULA gera importantes flags de controle:

* Zero (Z)
* Overflow (O)

---

## Fluxo de Execução

```text
          ROM
           │
           ▼
 Program Counter (PC)
           │
           ▼
 Instruction Register (IR)
           │
           ▼
 Unidade de Controle
           │
   ┌───────┴────────┐
   ▼                ▼
  ULA             Memória RAM
   │
   ▼
Acumulador (AC)
```

---

## Arquitetura do Processador

<img width="1291" height="595" alt="Arquitetura do Processador" src="https://github.com/user-attachments/assets/36ef6a81-1dad-4a29-b89b-e5b6bae924cf" />

---

## Documentação

O documento contendo a especificação do processador pode ser encontrado abaixo:

**MPU_RISC_4BITS.pdf**

https://github.com/user-attachments/files/28653362/MPU_RISC_4BITS.pdf

---

## Objetivos do Projeto

* Compreender a arquitetura interna de um processador;
* Estudar o funcionamento da Unidade de Controle;
* Entender o papel da ULA e dos registradores;
* Explorar o ciclo de execução de instruções;
* Desenvolver programas em Assembly;
* Aprender conceitos fundamentais de Arquitetura e Organização de Computadores.

---

## Conteúdos Abordados

* Arquitetura Von Neumann
* Arquitetura Harvard
* CPU
* Registradores
* Program Counter (PC)
* Instruction Register (IR)
* Acumulador (AC)
* Unidade de Controle (UC)
* Unidade Lógica e Aritmética (ULA)
* Memória RAM
* Memória ROM
* Linguagem Assembly
* Modos de Endereçamento
* Ciclo de Instruções
* Organização de Computadores

---

<div align="center">

**Arquitetura e Organização de Computadores I**

Projeto acadêmico para estudo da implementação e funcionamento de um microprocessador didático.

</div>
