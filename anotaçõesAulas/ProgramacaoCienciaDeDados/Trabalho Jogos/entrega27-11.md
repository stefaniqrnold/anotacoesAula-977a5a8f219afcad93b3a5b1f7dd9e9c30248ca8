---
# configurações do marp
marp: true
theme: gradient
class:  
- blue # classe azul do tema
- lead # centralizar

paginate: true 

title: Análise da Duração de Jogos
description: slides para apresentação no dia 27/11/24 para a materia de Programação Pra Ciência de Dados
author: Stéfani Arnold
keywords: jogos, análise de dados

# canto dos slides
header: 'Aplicação de Técnicas de Ciência de Dados'

---
# **Aplicação de Técnicas de Ciência de Dados**
##  - Engenharia de Software e Ciência da Computação
### **Stéfani Arnold e Nicolas Hass**
### `Módulo 02/2024`

---
### Coisas que tivemos em aula e obrigatóriamente precisam estar no trabalho final, entrega dia 25/11 sem possibilidade de prorrogração. Não precisa apresentação em slides desde que seja apresentado o código, a coisa funcionando e saibamos explicar direito.

---
## Python3
Python 3 é o alicerce do projeto, utilizado para implementar e demonstrar as técnicas de ciência de dados. 
Sua versatilidade e uma vasta coleção de bibliotecas permitem abordar todas as etapas da análise, desde a manipulação até a visualização de dados. 

---
## Versionamento (Git/GitHub)
Git e GitHub auxiliam na organização e no versionamento. Com ambos, foi possível rastrear mudanças no código, criar ramificações para testar abordagens diferentes e corrigir erros de maneira segura. 

---
## Manipulação de Arquivos (Caso utilizar no trabalho manipulação de arquivos no trabalho) **[opcional escolher esse ou o outro]**
A manipulação de arquivos foi explorada com formatos como CSV e JSON, com o intuito de armazenar e processar dados coletados. O formato CSV foi utilizado para leitura e escrita de grandes volumes de dados tabulares, enquanto o JSON foi empregado para estruturar dados hierárquicos obtidos de APIs. 

---
## Orientação a Objetos
A aplicação da orientação a objetos (OO) neste projeto trouxe organização e modularidade ao código. Por exemplo, foram criadas classes para representar jogos e suas métricas, encapsulando atributos como título, gênero e tempo médio de jogo. Além disso, métodos foram implementados para calcular estatísticas ou converter dados entre formatos, promovendo a reutilização e a clareza do código.

---
## Manipulação de banco de dados
A manipulação de banco de dados foi uma etapa crucial para organizar e recuperar dados de maneira eficiente. Utilizamos SQLite para criar e consultar um banco de dados local contendo informações sobre jogos e seus respectivos tempos de duração. Com Python, foi possível integrar consultas SQL diretamente no fluxo de análise, facilitando a combinação de dados provenientes de múltiplas fontes.

---
## Análise e visualização de dados
A análise foi realizada explorando dados coletados sobre a duração de jogos, avaliando correlações com variáveis como gênero, número de vendas e avaliações. Ferramentas como Seaborn e Matplotlib foram empregadas para criar gráficos intuitivos, permitindo a visualização de tendências. Por exemplo, gráficos de dispersão ilustraram a relação entre duração média e popularidade dos jogos, enquanto histogramas ajudaram a identificar padrões gerais de tempo de jogo.

---
## Coleta de dados online (Caso utilizar no trabalho extração/obtenção os dados de forma online) **[opcional escolher esse ou o outro]**
A coleta de dados online foi realizada por meio de APIs públicas, como a API do Steam, e técnicas de web scraping, sempre respeitando as políticas de uso das fontes. Essa abordagem garantiu acesso a dados atualizados e relevantes sobre jogos, incluindo informações detalhadas que enriqueceram a análise e forneceram insumos para a modelagem.

---
## Técnicas de Manipulação de dados **(importante, precisa fazer. Mas só foi falado em um slide das aulas, então prestar atenção nessa)**
    As técnicas de manipulação de dados foram aplicadas para garantir que os dados fossem adequados à análise, seguindo estas etapas:

    Inspeção: Inicialmente, os dados foram avaliados para identificar valores ausentes, formatos inconsistentes e possíveis outliers.
    Limpeza: Foram removidos registros duplicados, corrigidos valores inconsistentes e tratados dados ausentes por meio de preenchimento ou exclusão estratégica.
    Transformação: Dados numéricos foram normalizados, enquanto categorias foram codificadas para facilitar o processamento.
    Modelagem: Os dados finais foram organizados em estruturas otimizadas para análise, como tabelas normalizadas e subconjuntos direcionados a perguntas específicas.

Esse processo foi essencial para garantir a precisão e a confiabilidade dos resultados apresentados.

---
## Conclusão

O trabalho final cumpriu os requisitos da disciplina de Programação para Ciência de Dados. Também consolidou nosso aprendizado em diversas áreas essenciais para a análise de dados. 

Ao aplicar os conteúdos estudados em aula conseguimos construir uma análise estruturada e relevante, que reflete tanto nosso progresso técnico quanto nossa capacidade de resolver problemas do mundo real.

O projeto proporcionou uma visão prática das etapas envolvidas em um ciclo completo de ciência de dados: da coleta à apresentação dos resultados.  
