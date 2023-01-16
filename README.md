# Polimi Recommender System challenge A.Y. 2022/23
This repo contains the code and the data used in [polimi's recsys challenge](https://www.kaggle.com/competitions/recommender-system-2022-challenge-polimi/overview)

## Results
Deadline 1
- Public leaderboard: 5th
- Private leaderboard: 1st

Deadline 2
- Public leaderboard: 2th
- Private leaderboard: 3th

MAP@10: 0.06200

## Best model
The final model is a hybrid recommender composed of
1. A hybrid recommender trained on a binary URM
2. A hybrid recommender trained on a real-valued URM
3. IALS on binary URM from Implicit's library

The first hybrid is composed of
- SLIM-ElasticNet (stacked URM)
- IALS
- MultVAE
- Mini hybrid of RP3Beta (user-similarity + item-similarity)
- EASE-R (weighted stacked URM)

The second hybrid is composed of
- EASE-R
- SLIM-ElasticNet
- RP3Beta (stacked)
- IALS_implicit
- MultVAE
