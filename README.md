# Algoritmos Computacionais: Álgebra Linear & Inteligência Artificial

Este repositório reúne um conjunto de soluções numéricas e lógicas implementadas em Python, voltadas para a resolução de sistemas lineares, problemas de otimização matricial, inteligência artificial e algoritmos baseados em restrições. 

O projeto conta com uma interface de entrada dinâmica via planilhas do Excel (`.xlsx`) através da biblioteca `pandas`, além de simulações embutidas para testes rápidos.

## 🛠️ Funcionalidades e Estrutura do Projeto

O código está dividido em quatro blocos de resoluções principais:

### 1. Álgebra Linear Computacional & Sistemas Lineares
*   **Fatorações Matriciais:** Implementação das decomposições **LU** e **QR** (via processo de ortogonalização de Gram-Schmidt).
*   **Métodos Diretos e Iterativos:** Resolução de sistemas lineares utilizando algoritmos de *Substituição para Frente* (Forward), *Substituição para Trás* (Backward), além dos métodos iterativos de **Jacobi** e **Gauss-Seidel** com critérios estritos de convergência.
*   **Análise Matricial:** Cálculo de Normas Matriciais e Normas Vetoriais.
*   **Condicionamento de Matrizes:** Análise de estabilidade numérica através do cálculo exato e estimado do Número de Condição.

### 2. Sudoku Computacional (Algoritmo de Restrição)
*   Resolução de tabuleiros clássicos 9x9 utilizando a técnica de força bruta com **Backtracking**.
*   Validação em tempo real das restrições fundamentais do jogo (linhas, colunas e subgrades 3x3).

### 3. Classificador KNN (K-Nearest Neighbors)
*   Algoritmo de aprendizado supervisionado para classificação de instâncias numéricas a partir de atributos e rótulos categóricos organizados em DataFrames.
*   Suporte para múltiplos cálculos de métricas de distância geométrica espacial e validação do hiperparâmetro *k*.

### 4. Análise de Autovalores e Métodos de Potência
*   Cálculo do polinômio característico de matrizes quadradas.
*   Implementação do **Método da Potência** para aproximação do autovalor dominante e seu respectivo autovetor associado.
*   Mecanismo de verificação matemática da validade de autovetores fornecidos pelo usuário.

## 🚀 Tecnologias Utilizadas

*   **Python 3**
*   **NumPy:** Manipulação matricial e operações vetoriais de alta performance.
*   **Pandas:** Mapeamento dinâmico e tratamento de dados de arquivos de entrada.

## ⚠️ Validações e Tratamento de Erros

O ecossistema possui tratamento robusto contra incongruências matemáticas e de formatação, interrompendo a execução com segurança ao detectar:
*   Matrizes não quadradas em métodos que exigem simetria.
*   Divergências de dimensão entre matrizes de coeficientes e vetores independentes.
*   Dados nulos (NaN), strings inválidas ou tabelas fora do padrão esperado.
*   Quebras de regras de tabuleiros de Sudoku ou falta de amostras mínimas para o KNN (*k*=3).
