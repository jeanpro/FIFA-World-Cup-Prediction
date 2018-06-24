# Projeto
__Objetivo__:
- Usar um modelo de redes neurais para prever os resultados da Copa do Mundo de 2018

Fonte: Linh Truong - https://github.com/mrthlinh/FIFA-World-Cup-Prediction

__Dados__: Os dados foram coletados de várias fontes como, por exemplo, Kaggle (a comunidade do Google para Data Scientists), site da FIFA e da EA games.

__Feature Engineering__: Para determinar quem tem mais chances de vencer, foram levados em conta 4 fatores:
1. Histórico de confrontos diretos.
2. Performance de ambos os times nos últimos 10 jogos.
3. O nível de aposta no site http://www.oddsportal.com/soccer/world/world-cup-2018/ para cada time (vitória, empate ou derrota).
4. O nível do time que foi à Copa do Mundo no video game (FIFA).


# Dados
### Fontes:
O dataset é composto de dados de jogos internacionais, resultados, níveis de aposta, ranking da FIFA, e nível do time no video game FIFA.
1. [FIFA World Cup 2018](https://www.kaggle.com/ahmedelnaggar/fifa-worldcup-2018-dataset/data)
2. [International match 1872 - 2018](https://www.kaggle.com/martj42/international-football-results-from-1872-to-2017/data)
3. [FIFA Ranking through Time](https://www.fifa.com/fifa-world-ranking/ranking-table/men/index.html)
4. [Bet Odd](https://www.kaggle.com/austro/beat-the-bookie-worldwide-football-dataset/data)
5. [Bet Odd 2](http://www.oddsportal.com)
6. [Squad Strength - Sofia](https://sofifa.com/players/top)
7. [Squad Strength - FIFA index](https://www.fifaindex.com/)



[1]: https://www.kaggle.com/ahmedelnaggar/fifa-worldcup-2018-dataset/data
[2]: https://www.kaggle.com/martj42/international-football-results-from-1872-to-2017/data
[3]: https://www.fifa.com/fifa-world-ranking/ranking-table/men/index.html
[4]: https://www.kaggle.com/austro/beat-the-bookie-worldwide-football-dataset/data
[5]: http://www.oddsportal.com
[6]: https://sofifa.com/players/top
[7]: https://www.fifaindex.com/

# Resultados preliminares

__Neural Net__: O modelo de redes neurais do autor mostrou-se com precisão de 60.80% no teste 10-fold CV.

|           Model         |10-fold CV error rate (%)|
|:-----------------------:|:-------------------:|
|Neural Net               |60.80|



### Resultados da Copa do Mundo 2018
Aplicando o modelo para os primeiros jogos da Copa na Rússia chegamos aos resultados abaixo. Enquanto o modelo não se mostrou tão preciso na fase de testes ele mostra resultados surpreendentes nos primeiros jogos da copa. Até o momento desta publicação foram 8 acertos em 14 jogos incluíndo jogos como __Portugal - Espanha (3-3)__, __Brasil - Suíça (1-1)__.

__Explicação dos resultados:__

Time A vs Time B

- "win_1": Time A vence com 1 gol de diferença.
- "win_2": Time A vence com 2 gols de diferença.
- "win_3": Time A vence com 3 ou mais gols de diferença.
- "lose_1": Time B vence com 1 gol de diferença.
- "lose_2": Time B vence com 2 gols de diferença.
- "lose_3": Time B vence com 3 ou mais gols de diferença.
- "draw_0": Empate

__Match Day 1__
![](https://github.com/mrthlinh/FIFA-World-Cup-Prediction/blob/master/pic/WC_2018_matchday1.PNG)

Accuracy = 8 / 16

__Match Day 2__
![](https://github.com/mrthlinh/FIFA-World-Cup-Prediction/blob/master/pic/WC_2018_matchday2.PNG)


# Referências
1. [A machine learning framework for sport result prediction](https://www.sciencedirect.com/science/article/pii/S2210832717301485)
2. [t-test definition](https://en.wikipedia.org/wiki/Student%27s_t-test)
3. [Confusion Matrix Multi-Label example](http://scikit-learn.org/stable/auto_examples/model_selection/plot_confusion_matrix.html#sphx-glr-auto-examples-model-selection-plot-confusion-matrix-py)
4. [Precision-Recall Multi-Label example](http://scikit-learn.org/stable/auto_examples/model_selection/plot_precision_recall.html#in-multi-label-settings)
5. [ROC curve example](http://scikit-learn.org/stable/auto_examples/model_selection/plot_roc.html#sphx-glr-auto-examples-model-selection-plot-roc-py)
6. [Model evaluation](http://scikit-learn.org/stable/modules/model_evaluation.html#precision-recall-f-measure-metrics)
7. [Tuning the hyper-parameters of an estimator](http://scikit-learn.org/stable/modules/grid_search.html)
8. [Validation curves](http://scikit-learn.org/stable/modules/learning_curve.html)
9. [Understand Bet odd format](https://www.pinnacle.com/en/betting-articles/educational/odds-formats-available-at-pinnacle-sports/ZWSJD9PPX69V3YXZ)
10. [EURO 2016 bet odd](http://www.oddsportal.com/soccer/europe/euro-2016/results/#/)
