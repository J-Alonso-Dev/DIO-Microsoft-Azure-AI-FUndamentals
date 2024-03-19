# Trabalhando com Machine Learning na Prática no Azure ML

## Passo a passo para a criação de um modelo de previsão com seus devidos pontos de extremidade configurados

Nesse primeiro Laboratório, usaremos um recurso de machine learning automatizado no Azure ML para treinar e avaliar um modelo de machine learning. Em seguida, faremos a implantação e testaremos o modelo treinado.

Para trabalhar no machine learn é essencial possuir um workspace e esta é a tarefa inicial, criar o workspace para assim poder criar o trabalho automatizado.

# Tutorial extraído da documentação oficial do Microsoft Learn :

# Criar um Workspace do Azure Machine Learning

Neste exercício, você criará um **Workspace do Azure Machine Learning**. O _Workspace_ é um ambiente colaborativo no qual você pode experimentar, treinar e implantar modelos de _machine learning_. Ele fornece recursos para gerenciar recursos de computação, armazenamento e serviços relacionados.

## Tarefas

1. Acesse o **Portal do Azure**.
2. No menu à esquerda, clique em **Criar um recurso**.
3. Na barra de pesquisa, digite **Machine Learning** e selecione **Machine Learning** nos resultados.
4. Clique em **Criar**.
5. Preencha os detalhes do _Workspace_:
    - **Nome do Workspace**: Escolha um nome exclusivo para o seu _Workspace_.
    - **Assinatura**: Selecione a assinatura do Azure.
    - **Grupo de Recursos**: Crie um novo grupo de recursos ou selecione um existente.
    - **Localização**: Escolha a região mais próxima de você.
    - **Versão do Azure Machine Learning**: Deixe como padrão.
    - **Plano de Armazenamento**: Escolha o plano de armazenamento adequado.
6. Clique em **Revisar + Criar** e, em seguida, em **Criar**.

Agora você tem um _Workspace do Azure Machine Learning_ pronto para ser usado! 🚀

Depois que nosso worlspace estiver pronto temos que entrar no ML studio para criar um "novo trabalho de ML automatizado"

# Usar Aprendizado de Máquina Automatizado para Treinar um Modelo

Neste exercício, você aprenderá a usar o **Aprendizado de Máquina Automatizado** para treinar um modelo. O Aprendizado de Máquina Automatizado (AutoML) é uma abordagem que permite que você treine modelos de machine learning sem a necessidade de ajustar manualmente hiperparâmetros ou escolher algoritmos específicos. Ele automatiza várias etapas do processo de treinamento, tornando-o mais eficiente e acessível.

Nesse caso, você usa um conjunto de dados de detalhes históricos de aluguel de bicicletas para treinar um modelo que prevê o número de aluguéis de bicicletas que deve ser esperado em um determinado dia, com base em características sazonais e meteorológicas.

## Tarefas

1. Acesse o **Portal do Azure**.
2. No menu à esquerda, clique em **Criar um recurso**.
3. Na barra de pesquisa, digite **Machine Learning** e selecione **Machine Learning** nos resultados.
4. Clique em **Criar**.
5. Preencha os detalhes do experimento de AutoML:
    - **Nome do Experimento**: Escolha um nome descritivo para o seu experimento.
    - **Assinatura**: Selecione a assinatura do Azure.
    - **Grupo de Recursos**: Crie um novo grupo de recursos ou selecione um existente.
    - **Localização**: Escolha a região mais adequada.
    - **Versão do Azure Machine Learning**: Deixe como padrão.
    - **Plano de Computação**: Escolha o plano de computação apropriado.
6. Clique em **Revisar + Criar** e, em seguida, em **Criar**.

Agora você está pronto para explorar o Aprendizado de Máquina Automatizado e treinar modelos de forma mais eficiente! 🚀

# Examinar o Melhor Modelo

Neste exercício, você aprenderá a examinar o melhor modelo treinado usando o **Aprendizado de Máquina Automatizado (AutoML)**. O AutoML é uma abordagem que automatiza várias etapas do processo de treinamento de modelos de machine learning, incluindo a seleção do melhor modelo com base em métricas de desempenho.

## Tarefas

1. Acesse o **Portal do Azure Machine Learning Studio**.
2. No menu à esquerda, clique em **Experimentos**.
3. Selecione o experimento que você criou anteriormente.
4. Na seção **Modelos**, clique no modelo com a melhor métrica de desempenho.
5. Explore as métricas, gráficos e detalhes do modelo para entender seu desempenho.
6. Se necessário, ajuste hiperparâmetros ou outras configurações para otimizar ainda mais o modelo.

Agora você está pronto para avaliar e aprimorar seus modelos de machine learning! 🚀

# Implantação e Teste do Modelo

Neste exercício, você aprenderá a implantar e testar um modelo de **Aprendizado de Máquina**. A implantação é uma etapa crucial para colocar seu modelo em produção e permitir que ele seja usado em cenários do mundo real.

## Considerações para Implantação

1. **Escolha o Método de Implantação Adequado**:

    - Existem dois métodos principais de implantação:
        - **Inferência em Tempo Real (Online)**: Processa dados de entrada à medida que são recebidos, com baixa latência. Ideal para aplicações que exigem respostas imediatas, como detecção de fraude ou sistemas de recomendação.
        - **Inferência em Lote (Offline)**: Processa um grande lote de dados de entrada de uma só vez, adequado para cenários de grande volume de dados.
    - O **Azure Machine Learning** usa **pontos de extremidade** para implantar modelos em cenários em tempo real e em lote.

2. **Garanta a Consistência**:

    - Implantar seu modelo de forma consistente em todos os ambientes (desenvolvimento, preparação e produção) é essencial.
    - Use tecnologias como **conteinerização ou virtualização** para fornecer consistência e encapsular o ambiente.

3. **Implante Atualizações Graduais**:
    - Utilize **atualizações de eliminação gradual** para garantir que o modelo tenha o desempenho esperado.
    - A estratégia de **distribuição segura** do Azure Machine Learning permite implantar um modelo em um ponto de extremidade, executar testes e aumentar gradualmente o tráfego para o novo modelo.

Agora você está pronto para explorar a implantação e testar seu modelo! 🚀

# Testar o Serviço Implantado

Neste exercício, você aprenderá a testar um serviço implantado usando o **Azure Machine Learning**. Testar o serviço é fundamental para garantir que ele funcione conforme o esperado antes de ser usado em produção.

## Etapas para Testar o Serviço Implantado

1. **Preparação dos Dados de Teste**:

    - Crie um conjunto de dados de teste representativo.
    - Garanta que os dados sejam semelhantes aos dados que o serviço encontrará em produção.

2. **Invocação do Serviço**:

    - Use o ponto de extremidade implantado para invocar o serviço.
    - Envie os dados de teste para o serviço e observe as respostas.

3. **Avaliação dos Resultados**:

    - Compare as previsões do serviço com os resultados esperados.
    - Verifique se o serviço está funcionando corretamente e se as métricas de desempenho estão dentro dos limites aceitáveis.

4. **Iteração e Ajustes**:
    - Se necessário, ajuste o modelo ou o serviço com base nos resultados dos testes.
    - Repita o processo até que o serviço esteja pronto para produção.

Agora você está pronto para testar seu serviço implantado e garantir sua eficácia! 🚀
