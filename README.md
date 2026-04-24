# Projeto: Simulação de Opinião Pública

**Abstract**. This study evaluates Large Language Models (LLMs) and supervised learning in simulating Brazilian public opinion on social inequality. Using CESOP-IPEC 04839 data (2,000 respondents), we employed Silicon Sampling by conditioning an LLM on sociodemographic profiles to predict responses. Random Forest achieved the best predictive performance among tested supervised algorithms. Results were assessed via point-to-point accuracy and Jensen-Shannon Distance (JSD). Analysis shows that while supervised learning excels at individual prediction, LLMs effectively mimic collective distributions, offering a robust alternative for social behavior studies and hypothetical research.

**Resumo**. Este estudo avalia Modelos de Linguagem de Grande Porte (LLMs) e aprendizado supervisionado na simulação da opinião pública brasileira sobre desigualdade. Utilizando dados da pesquisa CESOP-IPEC 04839 (2.000 respondentes), aplicou-se Silicon Sampling para condicionar um LLM a perfis sociodemográficos. O Random Forest obteve o melhor desempenho entre os algoritmos supervisionados. Os resultados foram validados via acurácia e Distância de Jensen-Shannon (JSD). A análise revela que, embora o aprendizado supervisionado supere na predição individual, os LLMs mimetizam eficazmente as distribuições coletivas, servindo como alternativa robusta para estudos de comportamento social e cenários hipotéticos.

## Grupo
1. Ana Beatriz Rocha Ribeiro
2. Maria José Pereira da Silva

## Arquivos de entrega: 
* [Código do projeto - Google Colab](https://colab.research.google.com/github/Projeto-MLG/Simulacao-de-Opiniao-Publica/blob/main/Projeto_MLG_Opinião_Pública.ipynb)
* [Artigo: Comparação entre Modelos Supervisionados e LLMs na Simulação de Respostas em Pesquisas de Opinião](Projeto_MLG_Artigo.pdf)
* [Apresentação em vídeo - YouTube](https://youtu.be/jey9ZktKqOA)
* [Arquivo da Apresentação - PowerPoint](Arquivos/MLG_Projeto_Desigualdade.pdf)

## Arquivos base: 
* [Base de Dados](Dataset/04839.sav)
* [Questionário](Dataset/quest_04839.pdf)
* [Distribuição das respostas](Dataset/TF_04839.pdf)

## Respostas geradas pela LLM: 
* [Arquivo formato csv](LLM_Generated_Answers/Base_teste_LLM.csv)
* [Arquivo com os prints das respostas do LLM](LLM_Generated_Answers/Prints_das_respostas_do_LLM.pdf)

## Referência:
* [Simulating Public Opinion: Comparing Distributional and Individual-Level Predictions from LLMs and Random Forests](Arquivos/entropy-27-00923.pdf)


