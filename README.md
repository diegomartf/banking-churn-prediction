# Previsão de Churn de Clientes Bancários

## Descrição do Projeto
Este projeto tem como objetivo analisar a taxa de churn (desistência) de clientes de uma instituição bancária. Utilizando um dataset contendo informações sobre clientes e seus comportamentos, foram desenvolvidos três modelos diferentes para prever quais clientes estão propensos a encerrar suas contas no banco.

Os três modelos utilizados são:

- **K-Nearest Neighbors (KNN)**
- **Regressão Logística**
- **Árvore de Decisão**
Cada modelo foi avaliado em termos de acurácia, precisão, recall, e curva ROC-AUC, com o objetivo de identificar qual deles oferece a melhor performance para esse problema específico.

## Dataset
O dataset utilizado contém as seguintes features:

- *RowNumber:* Número sequencial da linha no dataset.
- *CustomerId:* Identificador único de cada cliente.
- *Surname:* Sobrenome do cliente.
- *CreditScore:* Pontuação de crédito do cliente.
- *Geography:* Localização geográfica do cliente.
- *Gender:* Gênero do cliente.
- *Age:* Idade do cliente.
- *Tenure:* Número de anos que o cliente está no banco.
- *Balance:* Saldo da conta do cliente.
- *NumOfProducts:* Número de produtos bancários que o cliente possui.
- *HasCrCard:* Indica se o cliente possui um cartão de crédito (Sim/Não).
- *IsActiveMember:* Indica se o cliente é um membro ativo (Sim/Não).
- *EstimatedSalary:* Salário estimado do cliente.
- *Exited:* Indica se o cliente encerrou sua conta no banco (Sim/Não).

## Modelos e Avaliação
### 1.  K-Nearest Neighbors (KNN)
O modelo de KNN foi o mais simples dos três. Ele atribui uma classe ao cliente baseado nas classes dos vizinhos mais próximos. Embora seja fácil de implementar, o KNN pode ser sensível a outliers e pode não performar bem em datasets com alta dimensionalidade.

Resultados:

- Acurácia: 81.8%
- ROC-AUC-SCORE: 78.1%
- Análise: O modelo de KNN não performou tão bem quanto os outros, provavelmente devido à sua natureza simplista e à falta de capacidade para capturar a complexidade do dataset.

### 2. Regressão Logística
A regressão logística foi aplicada como um modelo baseline devido à sua simplicidade e interpretabilidade. Ela modela a relação entre as features e a probabilidade de churn utilizando uma função sigmoide.

Resultados:

- Acurácia: 81.3%
- ROC-AUC-SCORE: 77.7%
- Análise: A Regressão Logística apresentou uma performance razoável, conseguindo capturar padrões lineares no dataset. Entretanto, pode ter dificuldade em capturar relações não lineares mais complexas.

### 3. Árvore de Decisão
O modelo de Árvore de Decisão foi escolhido por sua capacidade de capturar interações não lineares entre as features. Ele cria uma série de regras de decisão baseadas nas features do dataset, o que o torna poderoso para modelos interpretáveis e adequados para datasets com interações complexas.

Resultados:

- Acurácia: 85.4%
- ROC-AUC-SCORES: 85.8%
- Análise: A Árvore de Decisão apresentou o melhor desempenho entre os três modelos, possivelmente devido à sua capacidade de modelar interações complexas entre as variáveis. No entanto, pode haver risco de overfitting, o que precisa ser considerado.

## Conclusão
Após a análise, o modelo de Árvore de Decisão se destacou como o mais eficaz para prever o churn dos clientes bancários neste dataset específico. Embora a Regressão Logística seja uma boa baseline, e o KNN seja fácil de implementar, ambos foram superados pela Árvore de Decisão, que conseguiu capturar melhor a complexidade das relações entre as variáveis.

Esses resultados indicam que, para este dataset, modelos que conseguem lidar com interações não lineares e complexas tendem a performar melhor. Como próximos passos, poderia ser interessante explorar modelos mais avançados como Random Forests ou Gradient Boosting para ver se há melhorias adicionais na performance.
