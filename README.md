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
- Construção de 6 modelos de classificação: K-NN, Árvore de decisão, Floresta aleatória, Regressão logística, CatBoost e Naive Bayes;
- Uso de diferentes métricas para avaliar o desempenho do modelo, priorizando aquelas que dão maior peso à classificação de falsos positivos: acurácia, precisão, recall, F1, F2, ROC-AUC e PR-AUC;
- Uso da estratégia de validação cruzada estratificada aplicada aos dados de treino dos modelos;
- Comparação entre o efeito de diferentes normalizações, incorporadas em pipelines para evitar o vazamento de dados;
- Otimização de hiperparâmetros com a ferramenta OPtuna, utilizando 130 tentativas para cada modelo;
- Aplicação de ferramentas de redução de dimensionalidade dos dados por meio de PCA (Análise dos Componentes principais);
- Comparação entre os modelos construídos;
- Uso de diferentes estratégias de explicabilidade dos modelos: PDP, Importância por permutação, LIME, SHAP e explicações contrafactuais;
- Análises adicionais da robustez e estabilidade dos modelos construídos.

## Instruções para uso
<p align="justify"> 


## Bibliotecas utilizadas
Os códigos utilizados para a realização da atividade foram desenvolvidos na linguagem de programação Python (3.13.7), contando com as seguintes bibliotecas e seus usos:

- Pandas (2.3.3): 

- Seaborn (0.13.2): 

- Matplotlib.pyplot (3.10.6): 

- ucimlrepo: 

- O objeto "permutation_importance" da biblioteca Sklearn.inspection (1.7.2): 

- O objeto "train_test_split" da biblioteca Sklearn.model_selection (1.7.2):
- 
- O objeto "KNeighborsClassifier" da biblioteca Sklearn.neighbors (1.7.2): 

- O objeto "DummyClassifier" da biblioteca Sklearn.dummy (1.7.2):
- 
- Os objetos "accuracy_score", "confusion_matrix", "roc_auc_score", "precision_score", "recall_score", "f1_score", "roc_curve" da biblioteca Sklean.metrics:

- Os objetos "StandardScaler", "MaxAbsScaler", "MinMaxScaler", "OneHotEncoder" da biblioteca Sklearn.preprocessing:


## Conclusões e resultados

## Agradecimentos
Agradeço ao professor docente responsável por ministrar a disciplina de Aprendizado de Máquina no segundo semestre letivo do ano de 2026 e por todo o suporte oferecido durante o desenvolvimento desta atividade.

## Referências 

[1]

## Docente responsável
| <img loading="lazy" src="https://github.com/user-attachments/assets/17dfa7bf-5ca9-42df-b63e-917827fc6308" width=115><br><sub> [Prof. Dr. Daneiel Roberto Cassar](http://lattes.cnpq.br/1717397276752482) |
| :--: |

## Desenvolvedora
| <img src="https://github.com/AnaLuizaSilv.png" width=115><br><sub>[Ana Luiza de Lima Silva](https://github.com/AnaLuizaSilv)</sub> |
| :--: |
Ana Luiza de Lima Silva, estudante do primeiro semestre do bacharelado em Ciência e Tecnologia da Ilum escola de ciência
