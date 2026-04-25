# Comparação entre Modelos Supervisionados e LLMs na Simulação de Respostas em Pesquisas de Opinião

Este trabalho apresenta uma comparação entre um modelo supervisionado (Random Forest) e um Modelo de Linguagem de Grande Porte (LLM), utilizando o ChatGPT, na simulação de respostas de pesquisas de opinião pública sobre desigualdade social no Brasil.

A base utilizada foi a pesquisa CESOP-IPEC 04839, com 2.000 respondentes de diferentes regiões do país. A variável analisada foi a percepção sobre o aumento da fome e da pobreza na cidade dos entrevistados.

No modelo supervisionado, foram testados diferentes algoritmos de machine learning, sendo o Random Forest escolhido por apresentar melhor desempenho preditivo e maior estabilidade. Já no LLM, foi aplicada a técnica de Silicon Sampling, em que o ChatGPT recebeu perfis sociodemográficos individuais para gerar respostas simuladas de forma personalizada.

A comparação foi realizada utilizando o mesmo conjunto de teste, permitindo analisar diretamente a resposta real, a previsão do modelo supervisionado e a resposta gerada pelo LLM.

As principais métricas utilizadas foram acurácia, precision, recall, F1-score, matriz de confusão e Distância de Jensen-Shannon (JSD).

Os resultados mostraram que o Random Forest apresentou melhor desempenho individual, com maior acurácia, enquanto o LLM demonstrou maior capacidade de reproduzir a distribuição coletiva das respostas.

A principal conclusão é que os dois modelos podem ser utilizados de forma complementar: o modelo supervisionado é mais eficiente para prever respostas individuais, enquanto o LLM apresenta maior potencial para simular padrões coletivos de comportamento social.

## Autores
1. Ana Beatriz Rocha Ribeiro
2. Maria José Pereira da Silva

## Professor Orientador
* Rogério de Oliveira

## Arquivos de entrega: 
* [Código do projeto - Google Colab](https://colab.research.google.com/github/Projeto-MLG/Simulacao-de-Opiniao-Publica/blob/main/Projeto_MLG_Opinião_Pública.ipynb)
* [Artigo: Comparação entre Modelo Supervisionado e LLM na Simulação de Respostas em Pesquisas de Opinião](https://github.com/Projeto-MLG/Simulacao-de-Opiniao-Publica/blob/27f28dfb117d352e83e35ecb45c56f187fd5cf07/Simula%C3%A7%C3%A3o%20de%20Opini%C3%A3o%20P%C3%BAblica.pdf)
* [Apresentação em vídeo - YouTube](https://youtu.be/jey9ZktKqOA)
* [Arquivo da Apresentação - PowerPoint](Arquivos/MLG_Projeto_Desigualdade.pdf)

## Arquivos base: 
* [Base de Dados](Dataset/04839.sav)
* [Questionário](Dataset/quest_04839.pdf)
* [Distribuição das respostas](Dataset/TF_04839.pdf)

## Respostas geradas pela LLM: 
* [Arquivo formato csv](LLM_Generated_Answers/Base_teste_LLM.csv)
* [Arquivo com os prints das respostas do LLM](LLM_Generated_Answers/Prints_das_respostas_do_LLM.pdf)

## Referencia:
* [Simulating Public Opinion: Comparing Distributional and Individual-Level Predictions from LLMs and Random Forests](Arquivos/entropy-27-00923.pdf)


