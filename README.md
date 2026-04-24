# Comparação entre Modelo Supervisionado e LLM na Simulação de Respostas em Pesquisas de Opinião

**Abstract:** This study evaluates Large Language Models (LLMs) and supervised learning in simulating Brazilian public opinion on social inequality. Using CESOP-IPEC 04839 data (2,000 respondents), we employed Silicon Sampling by conditioning an LLM on sociodemographic profiles to predict responses. Random Forest achieved the best predictive performance among tested supervised algorithms. Results were assessed via point-to-point accuracy and Jensen-Shannon Distance (JSD). Analysis shows that while supervised learning excels at individual prediction, LLMs effectively mimic collective distributions, offering a robust alternative for social behavior studies and hypothetical research.

**Resumo:** Este estudo avalia Modelos de Linguagem de Grande Porte (LLMs) e aprendizado supervisionado na simulação da opinião pública brasileira sobre desigualdade. Utilizando dados da pesquisa CESOP-IPEC 04839 (2.000 respondentes), aplicou-se Silicon Sampling para condicionar um LLM a perfis sociodemográficos. O Random Forest obteve o melhor desempenho entre os algoritmos supervisionados. Os resultados foram validados via acurácia e Distância de Jensen-Shannon (JSD). A análise revela que, embora o aprendizado supervisionado supere na predição individual, os LLMs mimetizam eficazmente as distribuições coletivas, servindo como alternativa robusta para estudos de comportamento social e cenários hipotéticos.

**Problema de Pesquisa:** Pesquisas de opinião pública são fundamentais para compreender como diferentes grupos sociais percebem temas como desigualdade, pobreza e condições de vida. No entanto, levantamentos tradicionais costumam apresentar limitações como alto custo, tempo de aplicação e dificuldade de atualização constante.
Com o avanço dos Modelos de Linguagem de Grande Porte (LLMs), surgiu a possibilidade de simular respostas humanas a partir de perfis sociodemográficos específicos, abrindo novas possibilidades para estudos sociais e cenários hipotéticos.
Diante desse contexto, este projeto busca responder à seguinte questão:
Modelos supervisionados tradicionais e LLMs apresentam o mesmo desempenho na simulação de respostas de opinião pública?
A comparação entre essas abordagens permite avaliar não apenas a capacidade preditiva individual, mas também o nível de fidelidade na reprodução de padrões coletivos de comportamento social.

**Base de Dados:** A base utilizada neste estudo é proveniente da pesquisa “Levantar a Percepção dos Brasileiros sobre Temas Relacionados à Desigualdade”, realizada pelo CESOP (Centro de Estudos de Opinião Pública) em julho de 2023.
A pesquisa contou com 2.000 respondentes com 16 anos ou mais, distribuídos em todas as regiões do Brasil, utilizando uma amostra probabilística com representatividade estatística significativa.
Cada linha da base representa um respondente e contém variáveis sociodemográficas como:
* sexo,
* idade,
* escolaridade,
* raça/cor,
* religião,
* renda individual,
* renda familiar,
* região geográfica,
* condição do município (capital, interior ou periferia).

A variável alvo escolhida foi a questão P05:
“Na sua percepção, nos últimos 12 meses, o número de pessoas em situação de fome e pobreza na sua cidade aumentou ou não aumentou?”
Essa pergunta foi utilizada como base para comparação entre as respostas reais, as previsões do modelo supervisionado e as respostas geradas pelo LLM.

**Modelo Supervisionado:** Antes da definição final, foram testados diferentes algoritmos de machine learning:
* Random Forest
* Gradient Boosting Machines (GBM)
* K-Nearest Neighbors (KNN)
* Redes Neurais (MLPClassifier)

O Random Forest apresentou o melhor desempenho entre os modelos avaliados, com maior estabilidade e melhor capacidade de generalização.
Sua escolha foi motivada principalmente por:
* robustez estatística
* bom desempenho com variáveis categóricas
* capacidade de capturar padrões não lineares
* menor sensibilidade a overfitting
  
Por isso, ele foi selecionado como modelo principal para a comparação com o LLM.

**Abordagem com LLM**

A abordagem baseada em LLM utilizou o ChatGPT como simulador de respondentes virtuais.
Foi aplicada a técnica de Silicon Sampling, que consiste em condicionar o modelo com perfis sociodemográficos reais para que ele atue como um respondente sintético de alta fidelidade.
O prompt foi estruturado com base em:

*persona adoption
*backstory individual
*regras rígidas de resposta
*proibição de uso de conhecimento externo

Cada execução representava um único respondente, e o modelo deveria escolher apenas uma resposta entre as opções disponíveis, sem explicações adicionais.
Essa estratégia buscou reproduzir como uma pessoa com aquele perfil provavelmente responderia à pergunta da pesquisa.

**Métricas de Avaliação**

A comparação entre os modelos foi realizada utilizando diferentes métricas de desempenho.

As principais foram:

*Acurácia → proporção geral de acertos
*Precision → qualidade das previsões positivas
*Recall → capacidade de recuperação das classes corretas
*F1-score → equilíbrio entre precision e recall
*Matriz de Confusão → identificação dos principais erros de classificação
*Feature Importance → análise da importância das variáveis no Random Forest
*Distância de Jensen-Shannon (JSD) → comparação entre distribuições de respostas

Enquanto a acurácia mede o acerto individual ponto a ponto, a JSD permite avaliar a fidelidade distributiva, ou seja, o quanto os padrões coletivos de resposta se aproximam da distribuição real da pesquisa.

## Grupo
1. Ana Beatriz Rocha Ribeiro
2. Maria José Pereira da Silva
3. Rogério de Oliveira

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


