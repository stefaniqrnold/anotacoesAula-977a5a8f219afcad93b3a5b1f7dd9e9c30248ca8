# Trabalho Final - Aplicação com Apache Kafka

### Este repositório contém um trabalho desenvolvido para a disciplina de **Sistemas Distribuídos**, do curso de **Engenharia de Software**. 

#### O objetivo deste projeto é explorar o **Apache Kafka**, suas funcionalidades e potenciais aplicações em sistemas distribuídos, consolidando os conhecimentos adquiridos ao longo da disciplina.

## Informações Gerais  
- Autoria: **Stéfani Gabriele Arnold de Camargo** 
  - Email: `stefani.camargo@sou.unijui.edu.br`

- Data de entrega: 06/12/24

- Professor Orientador: MArcelo awadwkdnajbd kfwejkjbs
    - Email: `email`

- Módulo 02/2024

- Sexto semestre da Graduação em Engenharia de Software

---

## Objetivos  
1. Implementar um ambiente completo com Apache Kafka, configurado para explorar diferentes funcionalidades, como streams, clients e connectors.  

2. Demonstrar a criação e utilização de tópicos com múltiplos brokers, incluindo cenários de replicação e falha de nodos. 

3. Utilizar o Kafka para integração com outras ferramentas e sistemas, destacando as personalizações realizadas.  

4. Consolidar o aprendizado sobre sistemas distribuídos aplicados a um middleware de mensagens de alta performance.  

---

## Estrutura do Repositório  
- `ambiente/`: Scripts e arquivos de configuração utilizados para criação do ambiente Kafka.  

- `codigo_fonte/`: Implementações realizadas para produção e consumo de dados.  

- `documentacao/`: Relatório detalhado com os passos de execução e prints dos testes.  

- `README.md`: Este documento.  

---

# Descrição do Projeto  

### Instalação e Configuração do Ambiente  
O ambiente foi configurado no sistema operacional **Fedora**, utilizando:  

- **Apache Kafka**: Middleware de mensagens.  

- **Java 17**: Ambiente de execução necessário.  
  - Instalado com:
    ```bash
    sudo dnf install java-17-openjdk
    ```
- **Docker Compose**: Para orquestração de containers Kafka e Zookeeper.  
  - Instalado com:
    ```bash
    sudo dnf install docker-compose
    ```

### Passos Realizados  
1. **Criação do Ambiente:**
   - Configuração de 3 nodos, 3 brokers, 3 partições e fator de replicação de 3.  

   - Utilização de containers Docker para isolamento e gerenciamento dos serviços.

2. **Produção e Consumo de Mensagens:**
   - Teste em múltiplos cenários:
     - Todos os nodos ativos.
     - Falha de um nodo.
     - Adição de um novo nodo ao cluster.

   - Produção e consumo de dados em tópicos específicos, simulando eventos reais.

3. **Exploração de Funcionalidades Adicionais:**
   - **Streams:** Implementação de uma aplicação para processamento de dados em tempo real.  

   - **Clients:** Conexão com o Kafka utilizando a linguagem Python.  

   - **Connectors:** Integração com um banco de dados para leitura/escrita de eventos.  

4. **Demonstração de Leitura em Grupo:**
   - Configuração de grupos de consumidores para processamento distribuído de mensagens.

---

## Avaliação  
Conforme solicitado na disciplina, foram entregues os seguintes itens:  

1. **Instalação e Configuração do Ambiente**:  
   - Ambiente contendo múltiplos nodos, brokers e replicação.  

2. **Testes Realizados**:  
   - Produção e consumo de mensagens em diferentes cenários.  

3. **Relatório com Prints**:  
   - Demonstração dos passos realizados, incluindo:
     - Configuração do ambiente.
     - Testes com falhas e adição de nodos.
     - Leitura em grupo.  

4. **Código-Fonte e Personalizações**:  
   - Implementações realizadas para atender às exigências do trabalho.

---

## Agradecimentos  
Agradeço à orientação do professor e ao suporte dos colegas da disciplina, que contribuíram para o aprendizado e realização deste trabalho.
