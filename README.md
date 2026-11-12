# Detecção de Fraudes em Cartões de Crédito

Projeto de Ciência de Dados e Machine Learning desenvolvido como parte de um estudo prático de análise de dados, classificação e detecção de fraudes em transações financeiras.

## Objetivo

Desenvolver e avaliar modelos de Machine Learning capazes de identificar transações fraudulentas em cartões de crédito, considerando o desafio do desbalanceamento entre transações legítimas e fraudulentas.

## Tecnologias utilizadas

- Python
- Pandas e NumPy
- Matplotlib e Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost
- SHAP
- Jupyter Notebook

## Dataset

Foi utilizado o conjunto de dados público de transações com cartões de crédito:

[Credit Card Fraud Detection Dataset](https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv)

A variável `Class` representa a classificação da transação:
- `0`: transação legítima.
- `1`: transação fraudulenta.

## Etapas do projeto

1. Importação das bibliotecas e carregamento dos dados.
2. Análise exploratória dos dados (EDA).
3. Verificação de valores ausentes e registros duplicados.
4. Separação das variáveis preditoras e da variável-alvo.
5. Divisão dos dados em treinamento e teste, com estratificação.
6. Padronização das variáveis.
7. Tratamento do desbalanceamento com SMOTE, aplicado somente aos dados de treinamento.
8. Treinamento dos modelos de Regressão Logística, Random Forest e XGBoost.
9. Avaliação e comparação dos modelos.
10. Análise de curvas ROC, Precision-Recall e matrizes de confusão.
11. Análise de importância das variáveis e interpretabilidade com SHAP.

## Resultados

Comparação dos modelos desenvolvidos:

| Modelo | Acurácia | Precisão | Recall | F1-score |
|---|---:|---:|---:|---:|
| Regressão Logística | 97,41% | 5,78% | 91,84% | 10,88% |
| XGBoost | 99,71% | 35,68% | 87,76% | 50,74% |
| Random Forest | 99,95% | 86,81% | 80,61% | 83,60% |

### Análise dos resultados

O modelo Random Forest apresentou o melhor equilíbrio geral entre precisão e recall, alcançando F1-score de 83,60%.

O XGBoost também apresentou desempenho relevante, com recall de 87,76%, demonstrando capacidade de identificar grande parte das transações fraudulentas.

A Regressão Logística apresentou o maior recall, mas sua baixa precisão indica uma quantidade elevada de falsos positivos.

Os resultados demonstram a importância de avaliar diferentes métricas em problemas de classificação com classes desbalanceadas.

## Como executar o projeto

Clone o repositório:

```bash
git clone https://github.com/dairjoseadm-sys/deteccao-fraudes-cartao-credito.git
```

Entre na pasta:

```bash
cd deteccao-fraudes-cartao-credito
```

Crie e ative um ambiente virtual:

```bash
python -m venv .venv
```

No Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Inicie o Jupyter Notebook:

```bash
jupyter notebook notebooks/deteccao_fraudes.ipynb
```

## Estrutura do projeto

```text
deteccao-fraudes-cartao-credito/
│
├── imagens/
│
├── notebooks/
│   └── deteccao_fraudes.ipynb
│
├── .gitignore
├── requirements.txt
├── deteccao_fraudes.html
└── README.md
```

## Considerações finais

Este projeto proporcionou a aplicação prática de técnicas de análise exploratória, preparação de dados, balanceamento de classes, treinamento de modelos de classificação e interpretação de resultados.

O desenvolvimento permitiu comparar diferentes algoritmos e compreender os desafios envolvidos na identificação de fraudes financeiras utilizando Machine Learning.

---

**Projeto desenvolvido para fins educacionais e de portfólio em Ciência de Dados e Inteligência Artificial.**
