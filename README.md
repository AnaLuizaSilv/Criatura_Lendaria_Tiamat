<img width="3030" height="617" alt="Ilum_Horizontal_monocroma╠ütico branco com assinatura especial_sem fundo" src="https://github.com/user-attachments/assets/6b554e40-defc-485f-8aa4-fe50e052d3ed" />


# Criatura Lendária - TIAMAT 2026

<h1 align="center"> Comparações da identificação da natureza de tumores cancerígenos por diferentes modelos de aprendizado de máquina </h1>

**Aluna:** Ana Luiza de Lima Silva.

**Turma:** 2026

**Docente responsável:** Prof. Dr. Daniel Roberto Cassar

**Disciplina:** Aprendizado de máquina - 2° semestre de 2026.

**Instituição:** Ilum escola de ciência.

## Índice
<!--ts-->
* [Objetivo da atividade](##Objetivo-da-atividade)
* [Conjunto de dados](##Conjunto-de-dados)
* [Metodologias e análises empregadas](##Metodologias-e-análises-empregadas)
* [Instruções para uso](##Instruções-para-uso)
* [Bibliotecas utilizadas](##Bibliotecas-utilizadas)
* [Conclusões e resultados](##Conclusões-e-resultados)
* [Agradecimentos](##Agradecimentos)
* [Referências](##Referências)
* [Docente responsável](##Docentes-responsáveis)
* [Autoria](##Desenvolvedora)
<!--te-->

## Objetivo da atividade
<p align="justify"> Este repositório corresponde ao projeto final da disciplina de Aprendizado de Máquina, ministrada pelo professor Daniel R. Cassar durante o segundo semestre de 2026. Seu principal objetivo é consolidar os ensinamentos e aprendizados nos diferentes modelos de Aprendizado de Máquina apresentados durante a disciplina, bem como estratégias para sua validação, implementação e otimização.


## Conjunto de dados
<p align="justify"> O conjunto de dados utilizado para o desenvolvimento da atividade foi o "Breast Cancer Wisconsin (Diagnostic)", disponibilizado pelo Machine Learning Repository da UC Irvine. Nele, são apresentados 569 exemplos, dos quais 357 são tumores de mama benignos e 212 malignos, além de 30 atributos numéricos (ou quantitativos) contínuos, sem valores duplicados ou faltantes. As informações descritas correspondem a medições de 10 características dos núcleos celulares entre os participantes do estudo, sendo elas: raio, textura, perímetro, área, suavidade, compacidade, concavidade, pontos côncavos, simetria e dimensão fractal.


## Motivação do projeto
<p align="justify"> O câncer de mama é o câncer de maior quantidade de diagnósticos entre mulheres, tornando relevante o desenvolvimento de ferramentas eficazes para a identificação e classificação precoce dos tumores a fim de permitira condução correta de tratamentos. Nesse sentido, o presente trabalho se propõe a, com base em um repositório público, comparar a atuação de diferentes modelos de aprendizado de máquina e sua efetividade em identificar características comuns e capazes de distinguir tumores de natureza benigna e maligna.

  
## Metodologias e análises empregadas
- Realização de uma análise exploratória dos dados;
- Uso de estratégia de Holdout, separando os dados do conjunto em conjuntos de treino (90%) e teste(10%);
- Construção de um modelo Baseline a fim de estabelecer um meio de comparação com os demais modelos;
- Construção de 6 modelos de classificação: K-NN, Árvore de decisão, Floresta aleatória, Regressão logística, XGBoost e Naive Bayes;
- Uso de diferentes métricas para avaliar o desempenho do modelo, priorizando aquelas que dão maior peso à classificação de falsos positivos: acurácia, precisão, recall, F1, F2, ROC-AUC e PR-AUC;
- Uso da estratégia de validação cruzada estratificada aplicada aos dados de treino dos modelos;
- Comparação entre o efeito de diferentes normalizações, incorporadas em pipelines para evitar o vazamento de dados;
- Otimização de hiperparâmetros com a ferramenta OPtuna, utilizando 130 tentativas para cada modelo;
- Aplicação de ferramentas de redução de dimensionalidade dos dados por meio de PCA (Análise dos Componentes principais);
- Comparação entre os modelos construídos;
- Uso de diferentes estratégias de explicabilidade dos modelos: PDP, Importância por permutação, LIME, explicações contrafactuais e ALE.

## Instruções para uso
<p align="justify"> Todos os códigos necessários para a atividade encontram-se no notebook Jupyter intitulado "Tiamat".


## Bibliotecas utilizadas
Os códigos utilizados para a realização da atividade foram desenvolvidos na linguagem de programação Python (3.13.7), contando com as seguintes bibliotecas e seus usos:

- Numpy (2.2.6): utlizado para armazenar a manipular os dados em arrays, além de conduzir o cálculo de parâmetros estísticos como média, variância e desvio padrão.

- Pandas (2.3.3): utilizados para visualizar o conjunto de dados e os resultados obtidos em tabelas;

- O objeto "Path" da biblioteca Pathlib: utilizado para criar o caminho dos arquivos da otimizaçãod e hiperparâmetros com Optuna;

- O objeto "product" da biblioteca Itertools: utilizado para construir a combinação entre os modelos e suas condições de avaliação, sobretudo normalizadores;

- Matplotlib (3.10.6): utilizada para produzir as representações gráficas dos dados e resultados;

- Seaborn (0.13.2): utilizada para, em conjunto com o Matplotlib, facilitar a visualização dos gráficos;

- Ucimlrepo (0.0.7): utilizado para importar o conjunto de dados;

- Scikit-learn (1.7.2) e seus diferentes objetos: utilziados para criar pipelines, aplicar métricas de desempenho, estratégias de pré-processamento, construção dos modelos e ferramentas de explicabilidade PDP e Permutation importance;

- O objeto "XGBClassifier" da biblioteca "xgboost" (3.0.5): utilizado para construir o modelo XGBoost;

- Optuna (4.5.0): utilizada para realizar a otimização de hiperparâmetros;

- O objeto "LimeTabularExplainer" da biblioteca "lime.lime_tabular" (0.2.0.1): utilizada para implementar a ferramenta de explicabilidade LIME;

- Dice_ml (0.12): utilizada para produzir as Explicações Contrafactuais para cada modelo;

- O objeto "Ale" da biblioteca "PyALE" (1.2.0): utilizada para construir a ferramenta de explicabilidade ALE;

- O objeto "wilcoxon" da biblioteca "scipy.stats" (1.16.2): utilizado para implementar o teste de Wilcoxon pareado entre os modelos com seleção de atributos ou não;

- O objeto "sm" da biblioteca "statsmodels.api" (0.14.5): utlziado para investigar as relações entre os atributos e o target;

- O objeto "variance_inflation_factor" da biblioteca "statsmodels.stats.outliers_influence": utilizado para investigar a milticolinearidade entre as variáveis por meio do Fator de Inflação da Variância (VIF);

- O objeto "SimpleNamespace" da biblioteca "types": utilziado para agrupar os resultados e parâmetros dos modelos.

## Conclusões e resultados
O desenvolvimento deste trabalho permitiu investigar como diferentes modelos de Aprendizado de Máquina se comportam quando aplicados a problemas de classificação binária, nesse caso tumores mamários benignos e malignos. Ao decorrer das análises, foi possível observar que o desempenho dos classificadores não depende exclusivamente do algoritmo escolhido, mas também das estratégias de pré-processamento e seleção de hiperparâmetros durante o treinamento do modelo. Nesse sentido, os resultados obtidos demonstram a importância de conduzir uma avaliação abrangente, considerando diferentes abordagens e critérios, antes de determinar qual modelo mais se adequa ao problema em análise.

Inicialmente, a análise exploratória permitiu compreender melhor a estrutura e distribuição dos dados, além da identificação do desbalanceamento existente entre as classes de targets. Devido a isso, adotou-se durante todo o notebook uma métrica de desempenho capaz de refletir o comportamento dos modelos em relação à classe de interesse, os tumores malignos, sendo a F2-score escolhida.

A construção do modelo Baseline compôs uma referência inicial para a comparação dos demais classificadores construídos psoteriormente. O KNN, isoladamente, demonstrou alta sensibilidade à escala dos atributos, tendo seu desempenho altamente melhorado com a aplicação de normalizadores. No entanto, o mesmo não se aplica a modleos como Árvore de decisão e Floresta aleatória, cujos desempenhos permaneceram os mesmos independentemente de quais normalizadores lineares fossem aplicados.

A Regressão Logística e XGBoost apresentaram altos desempenhos após a otimização de hiperparâmetros, com F2-score de, aproximadamente, 97%, demonstrando que modelos relativamente simples são capazes de identificar os padrões presentes entre os dados.

Em uma comparação final após conduzir a implementação e otimização isolada de cada modelo e a seleção de atributos e redução de dimensionalidade, a Regressão Logística com seleção de atributos apresentou melhor desempenho médio, com F2-score de, aproximadamente, 97% e identificação incorreta de apenas 1 caso no conjunto de teste.

Em síntese, o presente trabalho permitiu compreender como a implementação e construção de modelos de Aprendizado de Máquina envolvem um processo contínuo de investigação e comparação, não apenas entre os modelos, mas também entre os parâmetros utilizados por estes e as estratégias de pré-processamento conduzidas. A implementação e análise conjunta de dados, algoritmos, métricas de desempenho, estratégias de otimização e ferramentas de explicabilidade empregados durante o trabalho contribuíram para produzir uma visão mais abrangente acerca de como cada uma dessas etapas pode contribuir para a construção final de um modelo e impactar em suas classificações.

## Agradecimentos
Agradeço ao professor docente responsável por ministrar a disciplina de Aprendizado de Máquina no segundo semestre letivo do ano de 2026 e por todo o suporte oferecido durante o desenvolvimento desta atividade.

## Referências 
[1] MINISTÉRIO DA SAÚDE. Câncer de mama. Disponível em: <https://www.gov.br/saude/pt-br/assuntos/saude-de-a-a-z/c/cancer-de-mama>. Acesso em: 1 nov. 2026.

[2] CABALLAR, Rina Diane; STRYKER, Cole. O que é desempenho do modelo? Disponível em: <https://www.ibm.com/br-pt/think/topics/model-performance>. Acesso em: 14 out. 2026.

[3] MARIANO, Diego. Métricas de avaliação em machine learning: acurácia, sensibilidade, precisão, especificidade e F-score. BIOINFO - Revista Brasileira de Bioinformática e Biologia Computacional, jul. 2021.

[4] CASSAR, Daniel R. ATP-203 1.1 - Tratamento de dados com pandas. 2026. Jupyter Notebook. Material didático não publicado.

[5] IBM. XGBoost. Disponível em: <https://www.ibm.com/br-pt/think/topics/xgboost>. Acesso em: 18 out. 2026.

[6] RCODER. Naive Bayes. Disponível em: <https://master-statistics.com/pt/aprendizado-de-maquina/naive-bayes/>. Acesso em: 18 out. 2026.

[7] CASSAR, Daniel R. ATP-203 8.0 - Redução de dimensionalidade com PCA. 2026. Jupyter Notebook. Material didático não publicado.

[8] CASSAR, Daniel R. ATP-203 8.1 - Seleção de Atributos. 2026. Jupyter Notebook. Material didático não publicado.

[9] 4.1. Partial Dependence and Individual Conditional Expectation plots. Disponível em: <https://scikit-learn.org/stable/modules/partial_dependence.html>. Acesso em: 1 nov. 2026.

[10] FEATURE IMPORTANCE. Permutation Importance | Feature Importance. Disponível em: <https://www.featureimportance.com/permutation-importance>. Acesso em: 1 nov. 2026.

[11] NASCIMENTO, Rodrigo. LIME: A Solução para Explicabilidade em Machine Learning. Disponível em: <https://conceitos.tech/tutoriais/inteligencia-artificial/machine-learning/o-que-e-lime-e-como-usa-lo-para-explicar-modelos-de-machine-learning/>. Acesso em: 1 nov. 2026.

[12] FURLANETTO, Gabriel. Câmpus de Rio Claro CausalBioCF: Contrafactuais Causais para Interpretabilidade de Modelos de Aprendizado de Máquina. Disponível em: <https://repositorio.unesp.br/server/api/core/bitstreams/ea1cd247-dd52-4b6b-9e97-4ba3bfbd23e2/content>. Acesso em: 1 nov. 2026.

[13] KIM, Seungjun Josh. Explainable AI (XAI) Methods Part 3 - Accumulated Local Effects (ALE) | Towards Data Science. Disponível em: <https://towardsdatascience.com/explainable-ai-xai-methods-part-3-accumulated-local-effects-ale-cf6ba3387fde/>. Acesso em: 1 nov. 2026.

## Docente responsável
| <img loading="lazy" src="https://github.com/user-attachments/assets/17dfa7bf-5ca9-42df-b63e-917827fc6308" width=115><br><sub> [Prof. Dr. Daneiel Roberto Cassar](http://lattes.cnpq.br/1717397276752482) |
| :--: |

## Desenvolvedora
| <img src="https://github.com/AnaLuizaSilv.png" width=115><br><sub>[Ana Luiza de Lima Silva](https://github.com/AnaLuizaSilv)</sub> |
| :--: |
Ana Luiza de Lima Silva, estudante do primeiro semestre do bacharelado em Ciência e Tecnologia da Ilum escola de ciência
