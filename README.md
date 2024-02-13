## Configurando uma Pesquisa com Azure AI Search

Este guia passo a passo fornecerá instruções detalhadas sobre como configurar uma pesquisa usando Azure AI Search, com insights adicionais sobre o processo e as possibilidades oferecidas por essa ferramenta.

## Passo 1: Criação de Recursos no Azure

### 1.1 Crie um recurso Azure AI Search

- Acesse o [Portal do Azure](https://portal.azure.com/).
- Clique em "+ Criar um recurso" e procure por "Azure AI Search".
- Configure o recurso com as seguintes configurações:
  - Assinatura: Sua assinatura do Azure.
  - Grupo de recursos: Selecione ou crie um grupo de recursos com um nome único.
  - Nome do serviço: Escolha um nome único.
  - Localização: Escolha qualquer região disponível.
  - Nível de Preços: Básico.
- Após a validação, clique em "Criar".

### 1.2 Crie um recurso Azure AI Services

- Retorne à página inicial do Portal do Azure.
- Clique em "+ Criar um recurso" e procure por "Azure AI Services".
- Configure o recurso com as seguintes configurações:
  - Assinatura: Sua assinatura do Azure.
  - Grupo de recursos: O mesmo grupo de recursos do seu recurso Azure AI Search.
  - Região: A mesma localização do seu recurso Azure AI Search.
  - Nome: Escolha um nome único.
  - Nível de Preços: Padrão S0.
- Após a validação, clique em "Criar".

### 1.3 Crie uma Conta de Armazenamento

- Retorne à página inicial do Portal do Azure.
- Clique em "+ Criar um recurso" e procure por "Conta de Armazenamento".
- Configure a conta de armazenamento com as seguintes configurações:
  - Assinatura: Sua assinatura do Azure.
  - Grupo de recursos: O mesmo grupo de recursos do seu recurso Azure AI Search e Azure AI Services.
  - Nome da conta de armazenamento: Escolha um nome único.
  - Localização: Escolha qualquer localização disponível.
  - Desempenho: Padrão.
  - Redundância: Armazenamento Redundante Localmente (LRS).
- Aguarde a implantação e acesse a conta de armazenamento.

## Passo 2: Extração e Armazenamento de Dados

### 2.1 Faça o upload dos documentos para o Azure Storage

- No menu à esquerda, selecione "Containers".
- Crie um novo container com o nome "coffeereviews" e nível de acesso público.
- Faça o download dos [coffee reviews](https://aka.ms/mslearn-coffee-reviews) e extraia os arquivos para a pasta "reviews".
- Selecione o container "coffeereviews" e faça o upload dos arquivos da pasta "reviews".

## Passo 3: Indexação dos Documentos

- No portal do Azure, acesse o recurso Azure AI Search.
- Na página Visão geral, selecione "Importar dados".
- Selecione "Azure Blob Storage" como a fonte de dados e configure os detalhes da fonte de dados.
- Na seção "Anexar Serviços Cognitivos", selecione o recurso Azure AI Services.
- Configure as habilidades de enriquecimento e salve as projeções no "knowledge store".
- Personalize o índice e o indexer de acordo com suas necessidades.
- Clique em "Enviar" para criar a fonte de dados, skillset, índice e indexer.

## Passo 4: Consulta do Índice

- Use o "Search explorer" para escrever e testar consultas.
- Selecione o índice "coffee-index".
- Escreva consultas JSON para recuperar documentos do índice.

## Passo 5: Revisão do Knowledge Store

- Volte para a conta de armazenamento no Azure portal.
- Selecione o container "knowledge-store" para revisar os dados enriquecidos.
- Explore os documentos e projeções armazenados no Knowledge Store.

## Insights e Possibilidades

- **Enriquecimento de Dados**: Use os serviços cognitivos do Azure para extrair informações valiosas dos documentos.
- **Consulta Avançada**: Aproveite a capacidade de escrever consultas complexas para recuperar informações específicas.
- **Aprendizado Automático**: Utilize os dados enriquecidos para treinar modelos de aprendizado de máquina e obter insights preditivos.
- **Integração de Ferramentas**: Integre o Azure AI Search com outras ferramentas e plataformas para criar soluções de pesquisa personalizadas.
- **Melhorar a Experiência do Cliente**: Essa solução pode ser utilizada para extrair insights valiosos das avaliações dos clientes, permitindo que a empresa melhore seus produtos e serviços.
- **Análise de Sentimento**: A análise de sentimentos pode ser útil para identificar tendências positivas e negativas nas avaliações dos clientes, auxiliando na tomada de decisões.
- **Identificação de Tópicos Relevantes**: A extração de frases-chave pode ajudar a identificar os tópicos mais discutidos pelos clientes, fornecendo direcionamento para futuras estratégias de negócios.

### Aprendizados Adquiridos

- **Integração de Serviços Azure**: A integração entre diferentes serviços do Azure para criar soluções de IA pode ser poderosa e eficaz.
- **Configuração de Indexação e Consulta**: A configuração de indexação e consulta em Azure AI Search pode ser simplificada com o uso de assistentes e interfaces intuitivas.
- **Exploração de Dados Enriquecidos**: O Knowledge Store oferece uma maneira conveniente de explorar e visualizar os dados enriquecidos extraídos dos documentos fonte.

Este guia fornece uma visão geral do processo de configuração de uma pesquisa com Azure AI Search, destacando os recursos e as etapas importantes envolvidas. Experimente explorar mais recursos e possibilidades oferecidos por essa poderosa ferramenta de pesquisa.
