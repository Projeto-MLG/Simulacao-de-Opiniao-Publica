Simulação de Opinião Pública com Modelo Supervisionado e LLM

1.	Objetivo
O objetivo deste projeto foi simular respostas de uma pesquisa de opinião pública utilizando duas abordagens: LLM e um modelo de aprendizado supervisionado. A ideia principal é comparar os resultados obtidos por cada método.

2.	Base de Dados
Foi utilizada uma base de dados de uma pesquisa sobre a percepção dos brasileiros em relação a temas de desigualdade social, disponibilizada pelo Centro de Estudos de Opinião Pública (CESOP). Essa base conta com aproximadamente 2.000 respondentes, distribuídos em diferentes regiões do Brasil.
Cada linha da base representa um indivíduo, contendo informações de perfil, como sexo, idade, escolaridade e renda, além das respostas dadas às perguntas do questionário.
Para este projeto, foi selecionada a questão P05 como variável alvo. Essa questão busca avaliar a percepção do respondente sobre o aumento da fome e da pobreza na sua cidade.

3. Metodologia
Inicialmente, os dados passaram por etapas de limpeza e organização, além da seleção das variáveis mais relevantes para o problema.
Para garantir que as respostas dos dois modelos fossem comparadas corretamente, foi criado um identificador único (id_respondente). Esse identificador foi utilizado apenas para manter o controle dos registros ao longo do processo.
Foi definido um conjunto de teste com pelo menos 200 respondentes. A partir desse mesmo conjunto, foram geradas, de forma individual, as respostas do LLM no ChatGPT, considerando o perfil de cada respondente separadamente. Em seguida, essas respostas foram incorporadas ao conjunto de teste utilizando o identificador criado, permitindo a comparação direta entre os dois modelos para os mesmos indivíduos. O prompt utilizado e os prints das respostas geradas nesse processo estão disponíveis no apêndice.
Para tornar os resultados mais estáveis e evitar que dependessem de uma única divisão dos dados, foi utilizada validação cruzada com 5 divisões (folds).

3.1 Modelos Testados
Antes da definição do modelo supervisionado, foram avaliados diferentes algoritmos de classificação com o objetivo de identificar a abordagem mais adequada para o problema.
Foram testados os seguintes modelos: Random Forest, K-Nearest Neighbors (KNN), Gradient Boosting Machines (GBM) e Rede Neural (MLPClassifier).
Os resultados indicaram que o Random Forest apresentou o melhor desempenho, com acurácia aproximada de 43,5%, seguido pelo GBM (42,0%), Rede Neural (38,5%) e KNN (33,5%).
Com base nesses resultados, o Random Forest foi selecionado como modelo supervisionado principal.

4.	Modelos Utilizados
Com base nos testes realizados,o modelo supervisionado escolhido foi o Random Forest.  Ele foi escolhido por ser um modelo robusto, capaz de lidar com diferentes tipos de variáveis e capturar padrões complexos nos dados (SILVA et al., 2023). 
Já o modelo baseado em LLM foi utilizado com o objetivo de simular respostas a partir do perfil dos respondentes. A ideia foi reproduzir, de forma aproximada, como uma pessoa com aquelas características poderia responder à pergunta, permitindo comparar esse comportamento com o modelo supervisionado.

5. Métricas de Avaliação
Para a comparação entre os modelos, foram utilizadas diferentes métricas, buscando analisar não apenas o desempenho geral, mas também o comportamento das previsões.
A acurácia foi adotada como medida principal, por indicar de forma direta a proporção de acertos do modelo. Também, foi analisado o relatório de classificação, que inclui métricas como precisão, recall e F1-score, permitindo uma avaliação mais detalhada para cada classe.
A matriz de confusão também foi utilizada com o objetivo de identificar os principais tipos de erro e entender como os modelos distribuem suas previsões entre as categorias.
No caso do modelo supervisionado, foi analisada a importância das variáveis, buscando identificar quais características dos respondentes tiveram maior influência nos resultados.
Por fim, a distância de Jensen-Shannon foi utilizada por permitir medir a diferença entre distribuições de probabilidade, sendo útil para comparar padrões de resposta entre os modelos (IA TRACKER, 2024).

6. Análise dos resultados
Os dois modelos foram avaliados usando o mesmo conjunto de teste, garantindo uma comparação justa.
De forma geral, o modelo supervisionado apresentou melhor desempenho em termos de acurácia, indicando maior capacidade de reproduzir os padrões observados nos dados.
Já o modelo LLM apresentou maior variação nas respostas, o que impactou a distribuição final. Isso mostra que ele simula respostas de forma diferente do modelo supervisionado, não seguindo exatamente os mesmos padrões observados na base.
A análise da importância das variáveis ajudou a entender quais características dos respondentes tiveram maior influência nas previsões do modelo supervisionado, contribuindo para uma melhor interpretação dos resultados.
Além disso, a distância de Jensen-Shannon permitiu quantificar a diferença entre as distribuições de respostas dos dois modelos, ajudando a avaliar o nível de aproximação entre eles.

6.1 Comparação entre os modelos
Além da análise textual, foi elaborada uma tabela comparativa com as principais métricas de desempenho dos modelos, facilitando a visualização das diferenças entre as abordagens.
Os resultados mostram que o modelo supervisionado apresentou melhor desempenho geral, com acurácia de 43,5%, enquanto o LLM obteve acurácia de 28,5%. Esse comportamento também se repete nas demais métricas, como precision, recall e F1-score.
Essa diferença indica que o modelo supervisionado consegue reproduzir com maior precisão os padrões presentes nos dados. Por outro lado, o LLM apresenta maior variação nas respostas, o que impacta diretamente seu desempenho e a distribuição final. 
O Gráfico 1 apresenta a comparação da acurácia entre os modelos, evidenciando o melhor desempenho do modelo supervisionado em relação ao LLM.
Grafico1: Comparação da acurácia entre os modelos (Supervisionado vs LLM)
 
Apesar do modelo supervisionado ter apresentado melhor desempenho, os valores de acurácia indicam que o problema ainda apresenta um nível considerável de dificuldade, possivelmente devido à natureza da variável alvo.

7. Conclusão
Os resultados mostram que tanto o modelo supervisionado quanto o LLM conseguem simular respostas de uma pesquisa de opinião, mas com comportamentos diferentes.
O modelo supervisionado teve melhor desempenho preditivo, enquanto o LLM apresentou maior variação nas respostas.
Isso indica que as duas abordagens podem ser usadas de forma complementar, unindo a capacidade de previsão com a simulação mais flexível baseada em linguagem.

8. Referências bibliográficas
https://iatracker.com.br/glossario/o-que-e-jensen-shannon-divergence/ 11/04/2026 às 17:59
SILVA, C. B. et al. Uma análise comparativa das técnicas de Machine Learning. Revista Apoena, 2023.
OPENAI. ChatGPT. Disponível em: https://chat.openai.com

9. Apêndice 
I – Prompt utilizado
Você deve atuar como um respondente simulado de uma pesquisa de opinião sobre desigualdade social no Brasil.
Cada execução corresponde a um respondente da base de dados. O perfil abaixo representa exatamente esse respondente e deve ser utilizado como única base para a decisão.
Sua tarefa é analisar o perfil e escolher exatamente uma opção de resposta para a pergunta abaixo.
Pergunta: Na sua percepção, nos últimos 12 meses, o número de pessoas em situação de fome e pobreza na sua cidade:
•	Aumentou → indique qual das frases abaixo melhor representa sua percepção
•	Não aumentou
Regras obrigatórias:
•	Considere apenas as informações do perfil fornecido.
•	NÃO utilize conhecimento externo ou suposições genéricas.
•	Escolha somente UMA opção.
•	NÃO invente respostas.
•	NÃO explique a escolha.
•	Retorne o número do id_ respondente e a resposta completa.
Opções de resposta:
1 = Tenho visto ou conheço muitas pessoas com dificuldades para comprar alimentos
2 = Tenho visto mais pessoas trabalhando nos semáforos/ruas
3 = Tenho visto mais favelas/barracos/áreas ocupadas
4 = Tenho visto o aumento da população em situação de rua/ pessoas morando na rua
5 = Não tenho percebido/ visto aumento de pessoas em situação de pobreza na cidade
6 = Não sabe/ Não respondeu
Perfil do respondente: 
Obs.: Aqui foi inserido o perfil a ser considerado para a simulação da resposta

