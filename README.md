# Universalizing Weak Supervision

![framework](assets/uws_figure.pdf)

This is the source code for our paper: Universalizing Weak Supervision. We propose a universal technique that enables weak supervision over any label type while still offering desirable properties, including practicalflexibility, computational efficiency, and theoretical guarantees



### System Requirements

* Anaconda
* Python 3.6
* Pytorch
* See environment.yml for details

### Environment Setup

We recommend you create a conda environment as follows

```
conda env create -f environment.yml
```

and activate it with

```
conda activate universalizing-weak-supervision
```

### Running Experiments

* Full ranking, partial ranking experiment
  * notebooks/{boardgames, movies}/RankingExperiments.ipynb
    * To play with configurations, you may look into configs {board-games, imdb-tmdb}_ranking_experiment.yaml
    * Mainly changed configurations are
      * n_train
      * n_test
      * p: null # 0.2 | 0.4 | 0.6 | 0.8 (observational probability)
      * num_LFs: 3 # 6 | 9 | 12
      * inference_rule: weighted kemeny # | snorkel | kemeny | pairwise_majority | weighted_pairwise_majority
        * Note that snorkel is our baseline. kemeny and pariwise_majority is a majority voting for full rankings, and partial rankings respectively.
* Regression experiment
  * notebooks/{boardgames, movies}/RegressionExperiments.ipynb
* Geodesic regression experiment
  * notebooks/geodesic-regression/geodesic_regression.ipynb
* Generic metric space experiment
  * notebooks/metric-spaces/generic_metric_spaces.ipynb 

