# 🔐 Primeiro Trabalho de Álgebra Linear — Código Secreto com Matrizes

## 📚 Descrição

Este projeto consiste em implementar, utilizando Python, um sistema de codificação e decodificação de mensagens baseado em **álgebra linear**, especificamente com o uso de **multiplicação de matrizes** e **matrizes inversas**.

A proposta foi desenvolvida como parte da disciplina de Álgebra Linear Algorítmica, sob orientação do professor Marcello Goulart Teixeira.

---

## 🧠 Objetivo do Trabalho

A ideia é transformar uma mensagem de texto (até 10 caracteres) em um vetor numérico e codificá-lo com o uso de uma matriz invertível `A`. O vetor resultante `b̄` é a mensagem cifrada. Para decifrá-la, deve-se reconstruir `A`, obter sua inversa `A⁻¹` via **método de escalonamento**, e aplicar:
$b = A^{-1}b̄$

---

## 🛠️ Como Funciona

### ✉️ Codificação

1. Cada caractere da mensagem é convertido em número:

   * Espaço = 0, A = 1, B = 2, ..., Z = 26 (sem acentos e pontuação).
2. A mensagem é convertida em um vetor coluna `b`.
3. Gera-se uma matriz `A` aleatória de dimensão `n × n` (3 ≤ n ≤ 10), com determinante ≠ 0.
4. Calcula-se o vetor codificado `b̄ = A·b`.

### 🧾 Decodificação

1. Com o vetor `b̄` e conhecendo a dimensão `n`, recria-se a matriz `A` usando a mesma regra.
2. Calcula-se a inversa de `A` com o **método de escalonamento**.
3. Aplica-se `b = A⁻¹·b̄` para obter o vetor original.
4. Converte-se novamente os números em caracteres para obter a mensagem original.

---

## 👨‍💻 Como Foi Implementado

O notebook foi desenvolvido seguindo as instruções propostas:

* Implementei funções para:

  * Conversão entre texto e vetor numérico.
  * Geração controlada de matriz `A` com garantia de invertibilidade.
  * Multiplicação de matriz para codificação.
  * Cálculo da inversa por escalonamento (sem usar bibliotecas externas).
  * Reconversão do vetor numérico para texto.
* Realizei testes com diferentes mensagens para validar a correta codificação e decodificação.
* Todas as operações matriciais foram feitas manualmente ou com auxílio do `NumPy`, exceto a inversão (que foi feita por escalonamento passo a passo).

---

## 🚀 Execução

Você pode executar o notebook em qualquer ambiente Jupyter (local ou online, como Google Colab). Basta seguir os passos do notebook, inserir a mensagem, e observar a codificação e decodificação em tempo real.

---


