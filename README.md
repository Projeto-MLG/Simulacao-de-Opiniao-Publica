# Projeto: Simulação de Opinião Pública

**Abstract**. This study investigates the capability of Large Language Models (LLMs) and supervised learning algorithms to simulate Brazilian public opinion regarding social inequality. Using data from the CESOP-IPEC 04839 survey, comprising a sample of 2,000 respondents, the methodology involved generating answers through an LLM conditioned on specific sociodemographic profiles to predict individual responses—a technique known as Silicon Sampling. Concurrently, various supervised algorithms were tested, with Random Forest achieving the best statistical performance. Results were evaluated through point-to-point accuracy and Jensen-Shannon Distance (JSD) to measure distributive fidelity. The comparative analysis revealed that while supervised learning is superior in individual prediction, the LLM demonstrates a robust ability to mimic the collective distribution of opinions, offering a promising alternative for social behavior studies and hypothetical research scenarios.

**Resumo**. Este trabalho investiga a capacidade de Modelos de Linguagem de Grande Porte (LLMs) e algoritmos de aprendizado supervisionado em simular a opinião pública brasileira sobre desigualdade social. Utilizando dados da pesquisa CESOP-IPEC 04839, com uma amostra de 2.000 respondentes, a metodologia consistiu em gerar respostas pelo LLM condicionadas a perfis socio-demográficos específicos para prever respostas individuais, técnica conhecida como Silicon Sampling. Paralelamente, diferentes algoritmos supervisionados foram testados, com o Random Forest apresentando o melhor desempenho estatístico. Os resultados foram avaliados por meio de acurácia ponto a ponto e da Distância de Jensen-Shannon (JSD) para medir a fidelidade distributiva. A análise comparativa revelou que, enquanto o aprendizado supervisionado é superior na predição individual, o LLM demonstra uma capacidade robusta de mimetizar a distribuição coletiva de opiniões, oferecendo uma alternativa promissora para estudos de comportamento social e cenários hipotéticos de pesquisa.

## Grupo
1. Ana Beatriz Rocha Ribeiro
2. Maria José Pereira da Silva

## Arquivos de entrega: 
* [Código do projeto - Google Colab](https://colab.research.google.com/github/Projeto-MLG/Simulacao-de-Opiniao-Publica/blob/main/Projeto_MLG_Opinião_Pública.ipynb)
* [Artigo: Simulação de opinião pública com modelo supervisionado e LLM](Projeto_MLG_Artigo.pdf)
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


