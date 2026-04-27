# Comparação entre Modelos Supervisionados e LLMs na Simulação de Respostas em Pesquisas de Opinião

Este projeto investiga a utilização de modelos supervisionados e Modelos de Linguagem de Grande Porte (LLMs) na simulação de respostas em pesquisas de opinião pública sobre desigualdade social no Brasil.

O estudo utiliza como base a pesquisa CESOP-IPEC 04839, composta por 2.000 respondentes distribuídos em diferentes regiões do país. A variável analisada corresponde à percepção dos entrevistados sobre o aumento da fome e da pobreza em suas cidades.

Na abordagem supervisionada, foram avaliados diferentes algoritmos de Machine Learning, como Random Forest, Gradient Boosting, KNN e Redes Neurais. O modelo Random Forest foi selecionado por apresentar melhor desempenho preditivo, maior estabilidade e melhor capacidade de generalização.

Na abordagem com LLM, foi aplicada a técnica de Silicon Sampling, utilizando o ChatGPT para simular respostas individuais a partir de perfis sociodemográficos reais. Cada respondente foi representado por uma persona estruturada com informações como sexo, idade, escolaridade, renda, região e religião, permitindo a geração de respostas contextualizadas.

A comparação entre os modelos foi realizada utilizando o mesmo conjunto de teste, garantindo equivalência na avaliação entre as respostas reais, as previsões do modelo supervisionado e as respostas geradas pelo LLM.

As métricas utilizadas incluíram:

* Acurácia
* Precision
* Recall
* F1-score
* Matriz de Confusão
* Feature Importance
* Distância de Jensen-Shannon (JSD)

Os resultados demonstraram que o Random Forest apresentou melhor desempenho na predição individual, com maior acurácia e maior consistência nas classificações. Por outro lado, o LLM apresentou maior proximidade com a distribuição coletiva das respostas, mostrando maior capacidade de simular padrões sociais agregados.

A principal conclusão do estudo é que as duas abordagens não são concorrentes, mas complementares: enquanto o modelo supervisionado se destaca na previsão individual, o LLM apresenta maior potencial para representar tendências coletivas e cenários hipotéticos em estudos de comportamento social.

## Autores
1. Ana Beatriz Rocha Ribeiro
2. Maria José Pereira da Silva

## Professor Orientador
* Rogério de Oliveira

## Arquivos de entrega: 
* [Código do projeto - Google Colab](https://colab.research.google.com/github/Projeto-MLG/Simulacao-de-Opiniao-Publica/blob/main/Projeto_MLG_Opinião_Pública.ipynb)
* [Artigo: Comparação entre Modelo Supervisionado e LLM na Simulação de Respostas em Pesquisas de Opinião](https://github.com/Projeto-MLG/Simulacao-de-Opiniao-Publica/blob/1b60014fa26624ef86eae5a9ca610346810082a7/Simula%C3%A7%C3%A3o%20de%20Opini%C3%A3o%20P%C3%BAblica.pdf)
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


