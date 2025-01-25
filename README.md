# Projeto de Análise e Previsão de Nota de Crédito 📊

Este projeto utiliza Python e aprendizado de máquina para prever as notas de crédito dos clientes (Boa, Regular, Ruim) com base em seus perfis e comportamentos de pagamento. A implementação utiliza a biblioteca **scikit-learn** para treinamento e avaliação de modelos, e inclui etapas para preparação dos dados, treinamento do modelo e previsões para novos clientes.

---

## Visão Geral do Projeto 📝

### Objetivos Principais:
1. **Compreender as Notas de Crédito dos Clientes**:
   - Analisar os dados dos clientes para identificar padrões que afetam a classificação da nota de crédito.

2. **Desenvolver um Modelo Preditivo**:
   - Treinar modelos de aprendizado de máquina para classificar as notas de crédito.
   - Selecionar o modelo com melhor desempenho para futuras previsões.

---

## Pré-Requisitos 🛠️

Certifique-se de que a versão necessária do Python e as bibliotecas estão instaladas antes de executar o script.

### Passos para Instalação 🖥️
1. **Instale o Python**:
   - Baixe e instale o Python no site oficial: [python.org](https://www.python.org). 🐍

2. **Instale as Dependências**:
   - Use o seguinte comando para instalar as bibliotecas necessárias:
     ```bash
     pip install pandas scikit-learn
     ```
   - Bibliotecas utilizadas:
     - `pandas`: Manipulação e limpeza de dados. 📊
     - `scikit-learn`: Treinamento e avaliação de modelos de aprendizado de máquina. 🤖

---

## Etapas do Script ⚡

1. **Importação e Preparação dos Dados**:
   - Carregue o conjunto de dados (`clientes.csv`) usando o `pandas`.
   - Aplique **Label Encoding** às variáveis categóricas, como:
     - `profissao` (Profissão)
     - `mix_credito` (Composição de Crédito)
     - `comportamento_pagamento` (Comportamento de Pagamento)

2. **Divisão Treino-Teste**:
   - Defina as features (`x`) e o alvo (`y`) para a previsão:
     - Coluna alvo: `score_credito`.
     - As features excluem colunas irrelevantes, como `id_cliente`.
   - Divida os dados em conjuntos de treinamento (75%) e teste (25%) usando `train_test_split`.

3. **Treinamento dos Modelos**:
   - Treine dois modelos de aprendizado de máquina:
     - **Random Forest Classifier**: Modelo baseado em árvores de decisão.
     - **K-Nearest Neighbors (KNN)**: Modelo de classificação baseado em distâncias.
   - Ambos os modelos são treinados no conjunto de dados de treinamento.

4. **Avaliação dos Modelos**:
   - Avalie a precisão de cada modelo usando `accuracy_score`:
     - Random Forest Classifier.
     - KNN Classifier.
   - Selecione o modelo com maior precisão (neste caso, **Random Forest Classifier**).

5. **Previsão para Novos Clientes**:
   - Carregue um novo conjunto de dados (`novos_clientes.csv`) contendo os perfis dos clientes.
   - Aplique as mesmas codificações para alinhar com os modelos treinados.
   - Preveja as notas de crédito dos novos clientes utilizando o melhor modelo.

6. **Visualização das Previsões**:
   - Exiba as previsões para os novos clientes, identificando a distribuição das notas de crédito.

---

## Resultados Esperados 🎯

- **Precisão do Modelo**:
   - Avaliar a porcentagem de previsões corretas para ambos os modelos.
- **Previsões**:
   - Uma lista de notas de crédito previstas (`Boa`, `Regular`, `Ruim`) para novos clientes com base em seus perfis.

---

## Observações ⚠️

- **Validação dos Dados**:
   - Certifique-se de que os conjuntos de dados (`clientes.csv` e `novos_clientes.csv`) estão corretamente formatados e sem valores ausentes.
- **Otimização do Modelo**:
   - O script utiliza hiperparâmetros padrão para os modelos; ajustes adicionais podem melhorar a precisão.
- **Escalabilidade**:
   - Considere implantar o modelo por meio de uma aplicação web ou desktop para previsões em tempo real.

---

## Melhorias Futuras 💡

1. **Engenharia de Features**:
   - Adicionar mais variáveis relevantes para melhorar o poder preditivo do modelo.

2. **Otimização de Hiperparâmetros**:
   - Ajustar os parâmetros dos modelos para melhorar a precisão, utilizando técnicas como grid search.

3. **Dashboard Interativo**:
   - Desenvolver um painel para visualizar previsões e tendências das notas de crédito.

4. **Integração com Sistemas de Negócios**:
   - Conectar as previsões do modelo a ferramentas de CRM para ajudar na tomada de decisões.

---

## Como Executar ⚙️

1. Coloque o script e os conjuntos de dados (`clientes.csv` e `novos_clientes.csv`) no mesmo diretório.
2. Execute o script em um ambiente Python (por exemplo, Jupyter Notebook, VS Code).
3. Siga as saídas passo a passo para analisar, treinar e prever.

---
