# Projecto_20
 
Predição de Adesão a Investimentos com Algoritmos de Machine Learning


Contextualização do Problema


Uma instituição financeira deseja entender o comportamento de seus clientes em relação a uma nova campanha de marketing voltada para investimentos. O objetivo é prever se um cliente aplicará seu dinheiro em um investimento baseado em dados históricos.

Este projeto utiliza diferentes algoritmos de Machine Learning para realizar a classificação e compara os desempenhos dos modelos através de métricas como acurácia, precisão, recall, f1-score e matrizes de confusão. A análise dos resultados tem como objetivo orientar a instituição na escolha do melhor modelo para previsões futuras e para uma tomada de decisão mais eficiente.


Objetivo do Projeto

Utilizar dados de campanhas anteriores para prever a probabilidade de um cliente investir.

Comparar diferentes algoritmos de classificação e identificar o modelo mais adequado ao problema.


Modelos Avaliados

Foram utilizados os seguintes algoritmos de Machine Learning:

Árvore de Decisão (sem normalização)

XGBoost Classifier (com normalização)

KNN (com normalização)

Random Forest (com normalização)

Logistic Regression (com normalização)

Support Vector Machine (SVM) (com normalização)


Discussão dos Resultados

1. Acurácia Geral dos Modelos:

O SVM foi o modelo com maior acurácia geral (73.82%), seguido de perto pela Logistic Regression (71.92%) e pela Árvore de Decisão (71.61%).

Modelos como XGBoost (71.29%) e Random Forest (70.35%) também apresentaram desempenhos competitivos.

O KNN teve o menor desempenho geral (68.77%), provavelmente devido à sua maior dependência de hiperparâmetros e sensibilidade a dados desequilibrados.

2. Análise de Verdadeiros Positivos (VP):

O XGBoost teve o maior número de verdadeiros positivos (85), mostrando que é eficaz em identificar os clientes que realmente investirão.

Random Forest (82) e SVM (72) também tiveram um bom desempenho em detectar investidores reais.

Logistic Regression apresentou o menor número de VPs (62), o que indica menor sensibilidade para identificar investidores.

3. Análise de Verdadeiros Negativos (VN):

Logistic Regression (166) e SVM (162) se destacam na identificação de clientes que não investirão, minimizando falsos positivos.

Modelos como Árvore de Decisão, XGBoost e Random Forest tiveram desempenho semelhante, com 141 verdadeiros negativos cada.

4. Falsos Positivos (FP) e Falsos Negativos (FN):

Logistic Regression teve o menor número de falsos negativos (25), sendo ideal para evitar perdas de investidores reais.

O XGBoost apresentou o menor número de falsos positivos (41), sugerindo maior confiabilidade ao identificar "não investidores".

O KNN e a Árvore de Decisão tiveram maior dificuldade neste aspecto, com FP (57 e 56, respectivamente).

5. Modelo com Melhor Equilíbrio:

O SVM oferece um bom equilíbrio entre detecção de investidores (VP = 72) e "não investidores" (VN = 162). Apresenta também uma acurácia consistente (73.82%).

Conclusão e Recomendção

Modelo Recomendado:

Com base nos resultados, o modelo Support Vector Machine (SVM) é recomendado por apresentar o melhor equilíbrio entre acurácia (73.82%), falsos positivos e falsos negativos. Ele é ideal para prever adesão a investimentos com maior precisão, evitando gastos desnecessários com "não investidores" e maximizando a captura de investidores reais.

Implicações para a Empresa:

Melhoria na Alocação de Recursos: O modelo pode ajudar a identificar clientes com alta probabilidade de investir, permitindo campanhas de marketing mais direcionadas.

Otimização de Custos: Minimizar falsos positivos reduz custos operacionais, enquanto minimizar falsos negativos evita a perda de investidores potenciais.

Próximos Passos:

Realizar validação cruzada para verificar a consistência do desempenho do modelo em diferentes subconjuntos de dados.

Ajustar hiperparâmetros do SVM para otimizar ainda mais o desempenho.

Implementar explicações de modelo (como SHAP) para entender melhor as variáveis mais influentes na decisão.

Referências

Os resultados e métricas foram baseados no desempenho obtido nos modelos treinados utilizando o dataset fornecido para o projeto. As métricas foram extraídas através de avaliações padronizadas como matriz de confusão, acurácia e f1-score.


Organização do Repositório notebooks/: Contém o notebook principal com a análise de dados e data/: Arquivo de dados em formato CSV para fácil acesso e replicação do projeto.





