
# Azure Cognitive Search: Aplicando AI Search para indexar e pesquisar dados

Desafio:
O objetivo é desenvolver uma pesquisa que interaja com um serviço de inteligência artificial para identificar palavras-chave, emoções, e também utilizar o serviço de armazenamento do Azure.

### Etapa 1: Configurando o recurso do Azure AI Search:

Clique no botão + Criar um recurso , pesquise Azure AI Search e crie um recurso Azure AI Search 

![alt text](<../../Imagens/01 - config da busca.gif>)

Após a conclusão da implantação, selecione Ir para o recurso

![alt text](<../../Imagens/02 - config do serviço de IA.gif>)

### Etapa 2: Configurando o armazenamento:

![alt text](<../../Imagens/03 - Criação do storage.gif>)

Clique em Revisar e em Criar. Aguarde a conclusão da implantação e vá para o recurso implantado.

Altere a configuração de Permitir acesso anônimo de Blob para Habilitado e selecione Salvar. Como demonstrado abaixo:

![alt text](<../../Imagens/05 - permitindo acesso anonimo de blob.gif>)


### Etapa 3: Configurando o Container:
No painel do menu esquerdo, selecione Containers 

![alt text](<../../Imagens/06 - criando container.gif>)

Adicionar as pesquisas que serão analisadas pelo AI SERVICE.

![alt text](<../../Imagens/07 adicionando pesquisas ao container.gif>)


Depois que o upload for concluído, você poderá fechar o painel Upload blob . Seus documentos estão agora em seu contêiner de armazenamento


### Etapa 4: Indexar os documentos

Depois de armazenar os documentos, você poderá usar o Azure AI Search para extrair insights dos documentos. O portal do Azure fornece um assistente de importação de dados . Com este assistente, você pode criar automaticamente um índice e um indexador para fontes de dados suportadas. Você usará o assistente para criar um índice e importar seus documentos de pesquisa do armazenamento para o índice do Azure AI Search.


### Etapa 5: Consultar um Índice

Use o Search Explorer para escrever e testar consultas. O explorador de pesquisa é uma ferramenta incorporada no portal do Azure que oferece uma maneira fácil de validar a qualidade do seu índice de pesquisa. Você pode usar o Search Explorer para escrever consultas e revisar resultados em JSON.

![alt text](<../../Imagens/04 - testando a pesquisa.png>)

### Conclusão Final

O Azure Cognitive Search é uma ferramenta altamente útil para indexação e consulta de dados, especialmente quando combinada com recursos avançados de AI Search. A capacidade de criar índices personalizados, integrar campos vetoriais e explorar diferentes funcionalidades oferecidas pela plataforma torna o processo de busca e recuperação de informações mais eficiente e adaptável às necessidades específicas de cada aplicação.