
# Trabalho Prático: UNO - Ordenação de Cartas Desordenadas

Este projeto foi desenvolvido como o Trabalho 3 da disciplina de Algoritmos e Estruturas de Dados 1 (AEDS 1) na Universidade Federal de Viçosa (UFV) - Campus Florestal. O objetivo principal foi implementar e analisar o desempenho de seis algoritmos de ordenação clássicos, aplicados à ordenação de cartas do jogo UNO, considerando cores e valores.

## 1. Descrição do Projeto
O software implementa a ordenação de uma mão de cartas do jogo UNO, representada por uma lista de cartas embaralhadas. Foram implementados seis algoritmos de ordenação: BubbleSort, SelectionSort, InsertionSort, ShellSort, QuickSort e HeapSort. O programa permite a análise comparativa do desempenho de cada algoritmo através de métricas como número de comparações, número de movimentações e tempo de execução.

## 2. Estrutura e Organização
O projeto foi organizado de forma modular para garantir a manutenibilidade e clareza do código, seguindo boas práticas de desenvolvimento de software:

* **Módulo Cartas**: Responsável por definir as propriedades das cartas do UNO, incluindo cores e valores, e gerenciar a criação do baralho.
* **Módulo Ordenação**: Implementa os seis algoritmos de ordenação com seus respectivos contadores de comparações e movimentações.
* **Módulo Menu**: Controla a interação com o usuário, oferecendo diferentes modos de entrada e opções de visualização.
* **Módulo Arquivo**: Responsável pela leitura de arquivos de entrada e processamento dos dados.

## 3. Funcionalidades

* **Modo Interativo**: Permite ao usuário visualizar a ordenação das cartas passo a passo, escolhendo qual algoritmo executar.
* **Modo Arquivo**: Processa múltiplos conjuntos de cartas a partir de um arquivo de texto, executando todos os algoritmos automaticamente.
* **Seis Algoritmos de Ordenação**: Implementação completa de BubbleSort, SelectionSort, InsertionSort, ShellSort, QuickSort e HeapSort.
* **Métricas de Desempenho**: Contabilização do número de comparações e movimentações realizadas por cada algoritmo.
* **Visualização Flexível**: Exibição das cartas ordenadas e das estatísticas de desempenho.

## 4. Algoritmos Implementados

### 4.1 BubbleSort
Algoritmo simples que percorre o vetor múltiplas vezes, comparando elementos adjacentes e trocando-os quando estão fora de ordem. Os elementos "borbulham" para suas posições corretas.

**Complexidade:** O(n²) no pior caso e O(n) no melhor caso.

### 4.2 SelectionSort
Baseia-se em selecionar o menor elemento da sequência e colocá-lo na primeira posição, depois o segundo menor na segunda posição, e assim sucessivamente.

**Complexidade:** O(n²) em todos os casos.

### 4.3 InsertionSort
Percorre o vetor da esquerda para a direita, inserindo cada elemento em sua posição correta entre os elementos já ordenados.

**Complexidade:** O(n²) no pior caso e O(n) no melhor caso (vetor já ordenado).

### 4.4 ShellSort
Uma melhoria do InsertionSort que permite trocas entre elementos distantes, utilizando uma sequência de intervalos decrescentes.

**Complexidade:** O(n²) no pior caso, mas pode chegar a O(n log² n) com boas sequências de intervalos.

### 4.5 QuickSort
Algoritmo de divisão e conquista que seleciona um pivô e particiona o vetor em elementos menores e maiores que o pivô, ordenando recursivamente cada partição.

**Complexidade:** O(n log n) no caso médio e O(n²) no pior caso.

### 4.6 HeapSort
Utiliza uma estrutura de dados heap (árvore binária) para ordenar os elementos. Primeiro constrói um heap máximo e então extrai repetidamente o elemento máximo.

**Complexidade:** O(n log n) em todos os casos.

## 5. Critérios de Ordenação das Cartas

As cartas do UNO são ordenadas considerando dois critérios em ordem de prioridade:
1. **Cor**: Seguindo a ordem: Vermelho, Amarelo, Azul, Verde
2. **Valor**: Números de 0 a 9, seguidos das cartas especiais (Bloqueio, Inverter, +2, Coringa, +4)

## 6. Compilação e Execução
O projeto utiliza um Makefile para facilitar o processo de compilação, gerenciando corretamente os arquivos distribuídos em diferentes pastas.

Para compilar e executar o projeto, execute os seguintes comandos no terminal:

```bash
make all
./programa