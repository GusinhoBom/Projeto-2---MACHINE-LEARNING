# Esteira de Aprendizado de Máquina: Car Evaluation Dataset

Este projeto apresenta uma esteira completa de aprendizado de máquina utilizando o dataset [Car Evaluation](https://archive.ics.uci.edu/dataset/19/car+evaluation) do UCI Machine Learning Repository.

## Objetivo

Prever a aceitabilidade de um carro com base em atributos como preço, manutenção, número de portas, capacidade, tamanho do porta-malas e segurança.

## Estrutura do Notebook

- **Importação de bibliotecas**
- **Carregamento e análise exploratória dos dados**
- **Pré-processamento** (tratamento de categorias, remoção de duplicatas)
- **Divisão dos dados** em treino, validação e teste
- **Treinamento e avaliação de modelo** (Regressão Logística)
- **Visualização dos resultados** (matriz de confusão, distribuição das classes)
- **Exemplo de predição**

## Como executar

1. Abra o notebook `gustavo_notebook.ipynb` em um ambiente Jupyter ou VSCode.
2. Execute as células sequencialmente.
3. Certifique-se de ter as seguintes dependências instaladas:
   - pandas
   - numpy
   - scikit-learn
   - matplotlib
   - seaborn

## Observações

- O dataset é carregado diretamente da internet.
- O pipeline utiliza codificação one-hot para variáveis categóricas.
- O modelo avaliado é uma Regressão Logística.
