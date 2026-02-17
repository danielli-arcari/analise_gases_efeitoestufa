# Análise de Emissões de Gases de Efeito Estufa no Brasil (1970–2021)

## Sobre o projeto

Este projeto foi desenvolvido como case prático no programa ONE G9 da Alura, onde assumi o papel de cientista de dados em um órgão de fiscalização ambiental.

O desafio era transformar uma base extensa de dados ambientais em informações claras que ajudassem na compreensão das dinâmicas de emissão de gases de efeito estufa no Brasil.

A proposta não era apenas explorar os dados, mas responder perguntas relevantes para apoiar decisões em políticas ambientais.

---

## Base de dados

Fonte oficial: SEEG (Sistema de Estimativa de Emissões e Remoções de Gases de Efeito Estufa)  
Plataforma: https://plataforma.seeg.eco.br/

**Dimensões do dataset:**

- 103.312 registros  
- 63 variáveis  
- Período de 1970 a 2021  
- 27 estados brasileiros  
- Setores econômicos: Agropecuária, Mudança de Uso da Terra e Floresta, Energia, Processos Industriais e Resíduos  
- Principais gases: CO₂, CH₄, N₂O e SF₆  

---

## Perguntas investigadas

- Como as emissões evoluíram ao longo das décadas?
- Quais estados apresentam maior volume de emissões?
- O tamanho da população explica o volume de emissões?
- Quais estados possuem maiores emissões per capita?

---

## Metodologia aplicada

- Transformação da base do formato wide para long utilizando `melt`
- Limpeza e padronização dos dados
- Agregações multidimensionais com `groupby`
- Cálculo de emissão per capita por estado
- Análise de correlação entre população e emissão total
- Visualizações com Matplotlib e Plotly

---

## Principais resultados

### Relação entre população e emissão

A correlação entre população e emissão total foi de **0,24**, indicando relação fraca.

Isso sugere que o volume populacional não é o principal determinante das emissões estaduais.

### Estados com maior emissão per capita

Os cinco estados com maior emissão per capita foram:

1. Roraima  
2. Rondônia  
3. Mato Grosso  
4. Pará  
5. Acre  

O padrão regional aponta forte influência de atividades relacionadas à agropecuária e mudança de uso da terra.

### Perfil estrutural das emissões

A análise por setor mostrou que o setor de **Mudança de Uso da Terra e Floresta** exerce papel central no volume total de emissões ao longo da série histórica.

---

## Tecnologias utilizadas

- Python 3  
- Pandas  
- NumPy  
- Matplotlib  
- Plotly  
- Google Colab  

---

## Conclusão

A análise evidencia que as emissões brasileiras possuem forte componente estrutural e setorial. Estados menos populosos podem apresentar emissões proporcionalmente maiores, reforçando que fatores econômicos e territoriais têm peso significativo.

O projeto demonstra aplicação prática de técnicas de manipulação, agregação e interpretação de dados com foco em geração de insights orientados à tomada de decisão.

---

## Autora

Projeto desenvolvido por Danielli Arçari como parte do programa ONE G9 da Alura.
