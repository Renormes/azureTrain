# azureTrain
train for Dio Azure AI-900

# Customer Churn Prediction

Este repositório contém um modelo de previsão de churn de clientes e os pontos de extremidade configurados para realizar previsões.

## Passo a Passo

### 1. Criar um Modelo de Previsão na Azure
1. Acesse o Azure Portal e faça login.
2. No painel esquerdo, clique em **Create a resource** e selecione **Machine Learning**.
3. Preencha os detalhes necessários, como nome do recurso, assinatura e grupo de recursos, e clique em **Create**.
4. Após a criação, vá para o recurso de Machine Learning e clique em **Launch studio**.

### 2. Carregar o Dataset
1. No Azure Machine Learning Studio, clique em **Datasets** no painel esquerdo.
2. Clique em **+ Create dataset** e selecione **From local files**.
3. Carregue o arquivo `Churn_Modelling.csv` e preencha as informações necessárias, como nome e descrição do dataset.
4. Clique em **Next** e configure as colunas do dataset conforme necessário.
5. Clique em **Create** para finalizar o carregamento do dataset.

### 3. Criar um Experimento de Machine Learning Automatizado
1. No Azure Machine Learning Studio, clique em **Automated ML** no painel esquerdo.
2. Clique em **+New automated ML run**.
3. Selecione o dataset que você carregou anteriormente (`Churn_Modelling.csv`).
4. Configure o experimento:
   - Nome do experimento: `ChurnPredictionExperiment`
   - Tipo de tarefa: **Classification**
   - Coluna de destino: `Exited`
5. Clique em **Next** e configure as opções de computação, como o cluster de computação a ser usado.
6. Clique em **Next** e revise as configurações do experimento.
7. Clique em **Finish** para iniciar o experimento.

### 4. Selecionar e Implantar o Melhor Modelo
1. Após a conclusão do experimento, vá para a seção **Models** no painel esquerdo.
2. Selecione o melhor modelo baseado nas métricas de avaliação (por exemplo, AUC, precisão).
3. Clique em **Deploy** para criar um endpoint.
4. Configure os detalhes do endpoint:
   - Nome do serviço: `ChurnPredictionService`
   - Tipo de serviço: **Azure Container Instance (ACI)**
5. Clique em **Deploy** para implantar o modelo.

### 5. Baixar o Arquivo JSON dos Pontos de Extremidade
1. No Azure Machine Learning Studio, vá para a seção **Endpoints** no painel esquerdo.
2. Selecione o endpoint `ChurnPredictionService` que você criou.
3. Clique em **Consume** para visualizar os detalhes do endpoint.
4. Clique em **Download Swagger JSON** para baixar o arquivo JSON dos pontos de extremidade.

---

Pronto! Você completou todas as etapas da atividade. Se precisar de mais alguma coisa, estou aqui para ajudar!
