# Análise de Emissões de Gases do Efeito Estufa no Brasil

## Sobre o Projeto

Este projeto apresenta uma análise detalhada dos dados de emissão de gases do efeito estufa no Brasil, utilizando a biblioteca Pandas para manipulação e exploração de dados. O trabalho foi desenvolvido como um case prático durante o curso One G9 da Alura, onde assumimos o papel de cientistas de dados em um órgão de fiscalização ambiental.

A proposta envolve responder perguntas críticas da equipe de supervisão através da criação de tabelas analíticas e visualizações que evidenciam padrões de emissão ao longo dos anos e entre diferentes setores econômicos brasileiros.

## Contexto do Case

A equipe de supervisão do órgão de fiscalização ambiental necessita compreender melhor as dinâmicas das emissões de gases causadores do efeito estufa em todo o país. Por isso, como cientistas de dados, fomos acionados para gerar insights que permitam orientar políticas ambientais e ações de controle de emissões.

As análises realizadas neste projeto utilizam dados oficiais do SEEG (Sistema de Estimativa de Emissões e Remoções de Gases de Efeito Estufa), que é a base de dados mais confiável e completa sobre o tema no Brasil.

## Fonte de Dados

Os dados utilizados provêm do SEEG, disponível no endereço: https://plataforma.seeg.eco.br/

Para acessar a base de dados:
1. Visite o site do SEEG
2. Clique em "Plataforma de dados"
3. Localize o arquivo de emissões por estado

O arquivo utilizado neste análise é: `SEEG10_GERAL-BR_UF_2022.10.27-FINAL-SITE.xlsx`

Este arquivo contém estimativas de emissões de gases do efeito estufa desagregadas por estado, setor econômico e tipo de gás, cobrindo o período de 1970 a 2021.

## Estrutura do Dados

O dataset original apresenta as seguintes dimensões:

**Dimensões Temporais**: Dados de 1970 a 2021, permitindo análises de tendências de longo prazo

**Dimensões Geográficas**: Todos os 27 estados brasileiros (26 estados + Distrito Federal)

**Dimensões Setoriais**: Atividades econômicas classificadas em níveis hierárquicos, incluindo Agropecuária, Mudança de Uso da Terra e Floresta, Energia, Processos Industriais e Resíduos

**Tipos de Gás**: Dióxido de Carbono (CO2), Metano (CH4), Óxido Nitroso (N2O) e Hexafluoreto de Enxofre (SF6)

**Categorias de Medição**: Emissões, remoções e bunker (combustíveis internacionais)

## Principais Insights do Dataset

### 1. Dominância do CO2 nas Emissões Totais

A análise revela que o dióxido de carbono é responsável pela maior parte das emissões totais de gases do efeito estufa no Brasil. Quando observamos o total acumulado ao longo de toda a série histórica, o CO2 se destaca significativamente em relação aos demais gases. Isso está diretamente relacionado à importância dos setores de energia e mudanças de uso da terra na economia brasileira.

### 2. Mudança de Uso da Terra como Principal Setor Emissor

O setor de "Mudança de Uso da Terra e Floresta" emerge como responsável pela maior quantidade de emissões totais. Este padrão reflete o impacto do desmatamento e das alterações nos ecossistemas florestais brasileiros. As flutuações nas emissões deste setor estão intimamente ligadas às variações nas taxas de desmatamento, particularmente na Amazônia.

### 3. Relevância da Agropecuária

A agropecuária se posiciona como um dos setores mais significativos em termos de emissões. As atividades de pecuária, especialmente a criação de gado, contribuem substancialmente para as emissões de metano. Este setor merece atenção especial nas políticas de redução de emissões, dado seu peso na economia brasileira.

### 4. Variações Regionais Importantes

Os estados apresentam perfis de emissão bastante distintos. Estados como Pará, Mato Grosso e Goiás, que possuem grandes áreas de atividade agropecuária e mudanças de uso da terra, apresentam emissões significativamente maiores que estados com menor atividade nestes setores.

### 5. Perfil Temporal das Emissões

A análise temporal mostra que as emissões não seguem um padrão linear. Há períodos de aumento e redução que refletem mudanças nas políticas ambientais, variações econômicas e alterações nas práticas agrícolas e florestais.

### 6. Multiplicidade de Gases com Contribuições Variadas

Embora o CO2 seja o gás mais abundante, os demais gases possuem contribuições relevantes quando consideramos seu potencial de aquecimento global. O metano, em particular, tem um potencial de aquecimento muito superior ao do CO2 em escalas de tempo de 100 anos, tornando as emissões de metano especialmente importantes nas estratégias de mitigação.

## Tecnologias Utilizadas

**Linguagem de Programação**: Python 3

**Ambiente de Desenvolvimento**: Google Colaboratory (Colab)

**Bibliotecas Principais**:
- Pandas: Manipulação, limpeza e análise de dados
- NumPy: Operações numéricas e cálculos
- Matplotlib: Visualização de dados em gráficos estáticos
- Plotly (opcional): Visualizações interativas mais avançadas

## Como Utilizar Este Projeto

### Pré-requisitos

Para executar este projeto, você precisará de:
- Conta Google (para acessar o Google Colaboratory)
- Acesso à base de dados SEEG ou arquivo Excel equivalente
- Conhecimento básico de Python e Pandas

### Passo a Passo para Execução

1. Acesse o Google Colaboratory em https://colab.research.google.com/

2. Crie um novo notebook ou carregue o arquivo `gases_estufa_Brasil.ipynb`

3. Faça upload do arquivo Excel do SEEG ou conecte sua conta do Google Drive

4. Execute as células do notebook em ordem sequencial

5. As análises serão exibidas como tabelas e gráficos interativos

### Estrutura do Notebook

O notebook está organizado em seções lógicas que seguem o fluxo natural da análise exploratória de dados:

**Importação de Bibliotecas**: Carregamento do Pandas e outras dependências

**Leitura dos Dados**: Importação do arquivo Excel contendo os dados do SEEG

**Exploração Inicial**: Análise da estrutura, dimensões e tipos de dados disponíveis

**Limpeza e Transformação**: Remoção de dados desnecessários, filtragem e transformação de formato dos dados

**Análise Exploratória**: Identificação de valores únicos, padrões e tendências

**Agregações e Visualizações**: Criação de tabelas resumidas e gráficos para responder às perguntas de negócio

## Análises Realizadas

O notebook implementa diversas técnicas de análise de dados:

**Filtragem Condicional**: Isolamento de dados por estado, setor ou tipo de gás para análises específicas

**Transformação de Formato**: Conversão do formato wide para long utilizando a função melt, facilitando análises por ano

**Agrupamento e Agregação**: Utilização de groupby para calcular totais e médias por diferentes dimensões

**Ordenação de Resultados**: Classificação dos dados para identificar os maiores emissores

**Visualização de Dados**: Criação de gráficos que facilitam a interpretação dos padrões identificados

## Exemplos de Consultas Realizadas

O projeto responde a diversos tipos de perguntas:

Qual é o total de emissões por tipo de gás ao longo de toda a série histórica?

Quais estados da região sul apresentam as maiores emissões?

Como as emissões de "Mudança de Uso da Terra e Floresta" se comportaram no Amazonas?

Qual foi o valor máximo de emissão de agropecuária no Pará em 2021?

Como evoluíram as emissões totais ao longo dos anos por setor econômico?

## Insights Técnicos da Implementação

A implementação demonstra boas práticas de análise de dados com Pandas:

**Manipulação Eficiente de Colunas**: Seleção de ranges de colunas (1970:2021) para trabalhar com dados temporais

**Transformação de Dados**: Uso de melt para converter dados de formato tabular em formato analítico

**Operações Vetorizadas**: Aplicação de filtros e operações que aproveitam a natureza vetorizada do Pandas

**Métodos de Agrupamento**: Exploração das capacidades do groupby para análises multidimensionais

**Visualizações Nativas**: Integração com matplotlib para criar gráficos diretamente dos DataFrames

## Contribuindo com o Projeto

Se você deseja contribuir com melhorias, novas análises ou correções:

1. Faça um fork do repositório

2. Crie uma branch para sua contribuição (`git checkout -b feature/analise-nova`)

3. Commit suas mudanças com mensagens claras (`git commit -m 'Adiciona nova análise de emissões por setor'`)

4. Push para a branch (`git push origin feature/analise-nova`)

5. Abra um Pull Request descrevendo suas mudanças

Sugestões de melhorias incluem: análises comparativas entre estados, projeções futuras utilizando modelos de séries temporais, ou integração com APIs para dados mais atualizados.

## Limitações e Considerações

Este projeto trabalha com dados até 2021. Análises mais recentes devem considerar dados atualizados do SEEG.

A análise foca em emissões brutas sem considerar compensações por remoções de gases (sumidouros), que são relevantes para o cálculo de emissões líquidas.

Os dados refletem estimativas baseadas em metodologias científicas estabelecidas, não medições diretas em todas as fontes.

## Recursos Adicionais

Para aprofundar-se no tema:
- Documentação oficial do SEEG: https://seeg.eco.br/
- Documentação do Pandas: https://pandas.pydata.org/docs/
- Guia de Análise Exploratória de Dados: https://pandas.pydata.org/docs/user_guide/basics.html
- Tutorial de Google Colaboratory: https://colab.research.google.com/notebooks/welcome.ipynb

## Licença

Este projeto foi desenvolvido como atividade educacional do curso One G9 da Alura. O código está disponível sob licença MIT, permitindo uso, modificação e distribuição com as devidas atribuições.

## Autor

Desenvolvido como case prático do programa One G9 da Alura, focando no desenvolvimento de habilidades em análise de dados com Python e Pandas, como parte dos estudos de Danielli Arçari

## Contato e Perguntas

Para dúvidas, sugestões ou discussões sobre o projeto, abra uma issue no repositório ou entre em contato através dos canais de comunicação do projeto.

Agradecimentos especiais ao SEEG por disponibilizar dados de qualidade e à Alura pela oportunidade de aprendizado prático em análise de dados ambientais.
