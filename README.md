Link do vídeo - https://youtu.be/omiA0B14bCA

# 🚗 Classificação de Carros com Machine Learning

Este projeto utiliza o dataset **Car Evaluation** do UCI Machine Learning Repository para treinar um modelo de **classificação automática** da qualidade de carros com base em características como preço, número de portas, segurança, entre outros.

---

## 🧠 Objetivo

Prever a **aceitabilidade de um carro** (inaceitável, aceitável, bom ou muito bom) com base em atributos como:

- Preço de compra
- Custo de manutenção
- Número de portas
- Capacidade de passageiros
- Tamanho do porta-malas
- Nível de segurança

---

## 📁 Dataset

- **Fonte**: [UCI Machine Learning Repository - Car Evaluation](https://archive.ics.uci.edu/ml/datasets/car+evaluation)
- **Instâncias**: 1.728
- **Atributos**: 6 atributos categóricos + 1 variável alvo (`class`)
- **Classes**: `unacc`, `acc`, `good`, `vgood` (desbalanceadas)

---

## 🛠️ Tecnologias e Bibliotecas

- Python 3.x
- Pandas e NumPy
- Scikit-learn (Pipeline, LogisticRegression, OneHotEncoder)
- Matplotlib e Seaborn (visualização)

---

## 🧪 Pipeline de Machine Learning

1. **Carregamento dos dados**
2. **Tratamento da coluna `'doors'`**  
   → Substituímos `'5more'` por `'5'` para simplificar o pré-processamento.
3. **Remoção de duplicatas**
4. **Separação dos dados em treino (60%), validação (20%) e teste (20%)**
5. **Criação de pipeline com:**
   - `OneHotEncoder` para codificação de variáveis categóricas
   - `LogisticRegression` para classificação (com `max_iter=200`)
6. **Treinamento e avaliação do modelo**
   - Métrica principal: **acurácia**
   - Avaliação com matriz de confusão

---

## 📊 Resultados

- **Acurácia na validação**: ~X.XX (exemplo: `0.85`)
- **Acurácia no teste**: ~X.XX
- **Desbalanceamento de classes identificado**
  - A maior parte dos dados pertence à classe `unacc`
  - Recomenda-se usar `class_weight='balanced'` ou técnicas de reamostragem para melhorias futuras

---

## 📈 Visualizações incluídas

- Distribuição das classes (`class`)
- Gráficos de barras para cada atributo categórico
- Matriz de confusão (heatmap)

---

## 📌 Exemplo de predição

O modelo também pode fazer predições para novos carros. Exemplo:

```python
sample = X_test.iloc[[0]]
pipeline.predict(sample)
