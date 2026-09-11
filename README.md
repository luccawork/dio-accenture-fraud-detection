# dio-accenture-fraud-detection
Este projeto foi desenvolvido como parte do Curso - "Python para Análise e Automação de Dados" com o objetivo construir um sistema de ML capaz de identificar transações fraudulentas em cartões de crédito.

Desenvolvido por Lucas Rodrigues.

O objetivo vai ser desenvolver um modelo preditivo que consiga identificar transações legítimas e diferencia-las de transações fraudulentas. Será utilizado um dataset onde apenas 0,17% das transações são fraudes.

Fraudes em transações financeiras representam um problema _**Bi**_ lionário para as instituições. As perdas globais com fraudes em cartões são grandiosas e um número que já era grande está aumentando graças a presença da IA.

Defini alguns paramêtros que o sistema de detecção precisa atender:

1 - Analisar transações em tempo real.
2 - Minimizar falsos positivos (não bloquear compras legítimas obviamente).
3 - Maximizar a detecção de fraudes reais.
4 - Ser explicável, já que métricas sem explicações são apenas números sem sentido.
Dataset
Fonte utilizada no projeto: Credit Card Fraud Detection - Kaggle

O dataset contém transações de cartões de crédito europeus realizadas em SET/2013.

Característica / Valor
Total de transações = 284.807
Transações fraudulentas = 492 (0,17%)
Transações normais = 284.315 (99,83%)
Features = 30 variáveis
Target = Class (0=Normal, 1=Fraude)
Desafios Identificados:
Desequilíbrio:

Um modelo que acusa normalidade para todas as transações teria 99,99% de Accuracy, mas não teria utilidade.
Vamos utilizar as métricas mais comuns para o caso sendo elas: Accuracy, Precision, Recall e F1-score.
PCA

Graças a compressão de dados do PCA utilizando matemática para compilar os componentes principais das transações, as colunas V1 á V28 estão comprimidas e não é possível interpretá-las diretamente.
Apenas Time e Amount são interpretáveis
Custo dos erros

- Falso negativo = deixar passar uma fraude !!! custo altíssimo
- Falso positivo = bloquear compra legítima ! custo moderado (cliente insatisfeito)
Método
O projeto segue o fluxo padrão de um pipeline de Machine Learning:

Análise Exploratória (EDA) → Entender os dados
Pré-processamento → Preparar as features
Treinamento de Modelos → Logistic Regression, Random Forest, XGBoost
Avaliação Comparativa → Métricas adequadas para desbalanceamento
Explicabilidade (SHAP) → Entender as decisões do modelo
Tecnologias Utilizadas
Python
Pandas → Manipulação de dados
NumPy → Operações matemáticas
Scikit-learn → Machine Learning clássico
XGBoost → Gradient Boosting
SHAP → Explicabilidade de modelos
Matplotlib & Seaborn → Visualização de dados
