---
Header:
    Left: ""
    Right: ""
    Center: ""
Footer:
    Left: ""
    Right: ""
    Center: ""
---

# Análise da Duração de Jogos 
> Nicolas Soares, Stefani Arnold

### Objetivo
Aplicar técnicas de Ciência de Dados para analisar a correlação entre as avaliações, o número de vendas e o tempo de duração dos jogos, utilizando bibliotecas Python e consumo de APIs para a coleta de dados.

### Tema
Os jogos eletrônicos são uma das indústrias mais lucrativas do mundo, com um público diversificado e crescente. Com a crescente popularização desta indústria e consequente aumento no preço de jogos, surge a discussão da relevância e necessidade do tempo de duração dos jogos produzidos. Analisando dados sobre diferentes jogos, podemos identificar como fatores como o tempo de duração, as avaliações dos usuários e o número de vendas estão inter-relacionados e influenciam o sucesso de um título no mercado.

### Problema Proposto
1. **Como as avaliações e o tempo de duração influenciam as vendas de jogos?** – O problema investiga se há algum padrão entre a avaliação de um jogo, seu tempo médio de jogabilidade, e o número de vendas, buscando entender quais características mais impactam o sucesso de vendas.
   
2. **Quais são as tendências de avaliação ao longo do tempo?** – Este problema busca analisar se há mudanças nas preferências dos jogadores ao longo dos anos, observando se os jogos com maior tempo de duração, por exemplo, tendem a ser melhor avaliados ou se o público prefere jogos mais curtos.

3. **O tempo de duração dos jogos influencia as avaliações?** – O problema examina a relação entre o tempo médio de jogabilidade de um título e as notas recebidas dos usuários, considerando se jogos mais longos ou mais curtos tendem a receber avaliações mais altas.

### Abordagem Sugerida
1. **Coleta de Dados:** Obter um conjunto de dados sobre jogos (utilizando APIs de plataformas como Steam, Metacritic, HowLongToBeat, ou outros serviços que forneçam dados sobre vendas, avaliações e tempo de duração dos jogos).
   
2. **Limpeza e Tratamento de Dados:** Remover dados ausentes, padronizar as informações e transformar os dados textuais, como nomes de jogos ou descrições, em dados estruturados.

3. **Análise Exploratória:** Identificar padrões como a relação entre tempo de duração e avaliação, quais jogos são mais vendidos por ano, ou a tendência das avaliações ao longo dos anos.

4. **Aplicação de Modelos:** Se possível, aplicar um modelo de regressão ou correlação para prever o sucesso de um jogo (avaliado por vendas ou notas) com base em suas características, como tempo de duração e avaliação dos usuários.