# Apache Kafka e Trabalho em Sistemas Distribuídos

## Autora: Stéfani Gabriele Arnold de Camargo
##

**Sistema Operacional:** Fedora  
As instruções foram adaptadas para o uso do Fedora, utilizando o gerenciador de pacotes `dnf` e ferramentas compatíveis.

---

## Exercício 1: Atividade Apache Kafka com KRaft

### Passos para Realização
1. **Preparação do Ambiente:**
   - Acesse a [documentação do Kafka](https://kafka.apache.org/documentation/#quickstart), seção 1.3: *Quick Start*.
   - Certifique-se de que o Java está instalado:
     ```bash
     sudo dnf install java-17-openjdk
     ```
   - Confirme a instalação:
     ```bash
     java -version
     ```

2. **Configuração e Execução:**
   - Complete os passos 1 a 6 do Quick Start. 
   - Para o passo 2, siga as instruções específicas de *Kafka with KRaft*.

3. **Testes e Prints:**
   - Execute os passos:
     - **Passo 4**: Escrevendo um registro no tópico.
     - **Passo 5**: Recebendo um registro do tópico.
     - **Passo 6**: Transferindo o conteúdo de um arquivo para um tópico.
   - Capture prints das saídas e organize-os em uma pasta no GitHub com o formato:
     ```
     ex_12_kafka/[seu_nome]
     ```

4. **Responda ao Quiz:**
   - Complete o questionário disponível em [https://forms.gle/XVmfxWG33XVfwdwt9](https://forms.gle/XVmfxWG33XVfwdwt9).

---

## Exercício 2: Execução com Zookeeper e Docker Compose

### Passos para Realização
1. **Execução Manual com Zookeeper:**
   - Baixe e configure o Kafka conforme as instruções da seção 1.3 do Quick Start.
   - Realize os seguintes passos:
     - Inicie o Zookeeper:
       ```bash
       bin/zookeeper-server-start.sh config/zookeeper.properties
       ```
     - Crie brokers e configure múltiplos brokers alterando propriedades como:
       ```properties
       broker.id=3
       listeners=PLAINTEXT://:9003
       log.dir=/tmp/kafka-logs3
       ```
     - Teste criação, produção e consumo de tópicos.

2. **Execução com Docker Compose:**
   - Instale o Docker Compose:
     ```bash
     sudo dnf install docker-compose
     ```
   - Baixe e configure o arquivo `docker-compose.yml` para executar o Kafka em containers.
   - Realize os seguintes testes:
     - Criação de tópicos com múltiplos fatores de replicação e partições.
     - Produção e consumo de mensagens.
     - Demonstração de grupos de consumidores.

3. **Encerramento:**
   - Garanta que todos os serviços sejam encerrados com os comandos:
     ```bash
     sudo docker-compose down
     ```

---

## Trabalho: Criação de Aplicação com Apache Kafka

### Passos para Realização
1. **Preparação do Ambiente:**
   - Configure o ambiente utilizando containers ou diretamente no host.
   - Garanta que o ambiente contenha:
     - **Nodos**: 3
     - **Brokers**: 3
     - **Partições**: 3
     - **Fator de replicação**: 3.

2. **Implementação da Aplicação:**
   - Explore funcionalidades avançadas:
     - **Streams**: crie aplicações para processar fluxos de dados.
     - **Clients**: conecte ao Kafka utilizando uma linguagem de programação (ex.: Python ou Java).
     - **Connectors**: integre o Kafka a bancos de dados ou diretórios de arquivos.
     - **Interfaces gráficas e personalizações** do Kafka.

3. **Teste e Demonstração:**
   - Execute os seguintes cenários:
     - Produção e consumo com todos os nodos ativos.
     - Produção e consumo com um nodo desativado.
     - Adição de um novo nodo.
     - Consumo em grupo.

4. **Documentação e Entrega:**
   - Organize no GitHub o diretório `Trabalho_5/[seu_nome]` contendo:
     - Arquivo `README.md` com:
       - Passos de instalação e execução.
       - Diferenças em relação ao exemplo de aula.
     - Código fonte completo.
     - Cinco prints de tela que demonstrem:
       1. Criação do ambiente.
       2. Produção e consumo com todos os nodos ativos.
       3. Produção e consumo com um nodo desativado.
       4. Adição de um novo nodo.
       5. Consumo em grupo.

5. **Prazo:**
   - Apresentação nos dias **06 e 13 de dezembro**.

---

## Considerações Gerais
- Certifique-se de que os pré-requisitos (Java, Docker e Docker Compose) estão instalados corretamente.
- Garanta que as configurações e testes sejam realizados com atenção.
- Organize os resultados e inovações no GitHub para facilitar a avaliação.
