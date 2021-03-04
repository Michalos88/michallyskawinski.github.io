# An Optimistic Perspective on Offline Deep Reinforcement Learning

Deep Learning is expressive function approximator that takes advantage of large amounts of data.

Most Deep RL agents architectures assume that agent will interact with a simulation, this limits the models to real-life applications. and might require to build a simulator, which might be costly.

Building simulators are expensive

Offline RL will deploying RL models cheaper and more generalizable.

Offline RL can help by either:

- Pretrain agents on logged data
- Evaluate RL aglos on basis of exploitation alone on a common datasets (like Imagenette)
- Deliver real-world impact

Offline RL is challenging due to distribution mismatch between online interaction and fixed logged dataset. - in other words RL will overfit offline dataset

Recent works has shown that standard Deep RL model underperform in offline settings and proposed regularizers to learned policies.

Rishabh paper investigates if standard off-policy RL can succedd in offline setting.

### Off-policy RL in Offline setting

**Dataset:** 60 Atari Games with 200 million frames each

**Number of Agents:** 5

**Agent**: DQN

They used sticky actions to make the problem more challenging with 25% probability.

They created 300 datasets, 5 per game, 200 million frames each.

Each dataset is 2.5x bigger than Imagenette.

There are charts that shows improvement on normalized scale. As shown in most case on-line dqn outperforms the off-line version, but in some cases off-line DQN outperforms on-line version with same amount of data and compute

However in case of distributional version of dqn (QR-DQN), the offline-version outperforms the on-line version in most of the games.

This demonstrates it's possible to train strong agents using off-line rl algorithms.

# Proposed improvements

Given that offline RL is trained on a fixed datasets, we can use the same techniques to improving generalization as in supervised ML

### Ensemble of Q-estimates:

Ensembling and dropout are widely used for improving generalization

Ensamble-DQN - trains multiple (linear) Q-estimates with different random initialization

Under version is REM DQN - Random Ensemble Mixture - minimize TD error on random convex combintations of multiple Q-estimates. Inspired by droput. Mutliple q-value estimates.

Offline REM outperforms on-line C51 and online DQN

With high number of gradient updates there is a large degradation of evaluated performance, which is equivalent to overfitting in supervised learning, that shows the need for ealry stopping or better regularization methods in offline rl.

# Remarks:

- Shows that offline-rl makes sense for diverse datasets, which kind of validates our approach
- Introduces ensembling for RL, are we doing ensambling with the various seeds?
- Proves the need for early-stopping in offline-rl
- Shows that off-line RL can actually outperform on-line RL for strong agents
