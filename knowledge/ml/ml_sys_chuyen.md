---
layout: default
title: ML System Design
---
<h1 class="page-title">Machine Learning Systems Design</h1>

### Table of Content:
<!-- 1. [Writing Cls](#writing-cls) -->
<!-- 2. [Writing CL descriptions](#writing-cl-descriptions) -->
<!-- 3. [Handling reviewers comments](#handling-reviewers-comments) -->

## ML System design in interviews
* Interviewers give you a problem, possibly related to their products, and ask you to **design a machine learning system to solve it.**
* This type of question has **become so popular that it's almost guaranteed that you'll be asked at least one** during your interview process. In an hour-long interview, you might have time to go over only one or two questions.
* Interviewers generally agree that even if you can't get to a working solution, as long as you communicate your thinking process to show that you understand different constraints, trade-offs, and concerns of your system, it's good enough.
* It's your job as the candidate to ask for clarification and narrow down the problem
* You drive the interview and **choose what to focus on.**
* What you choose to focus on speaks volumes about your interest, your experience, and your understanding of the problem.
* Many candidates don't even know what a good answer looks like. It's not taught in school. If you've never deployed a machine learning system to users, you might not even know what you need to worry about when designing a system.
* "When I ask such questions, what I am looking for is the following
  * Can the candidate break down the open ended problem into simple components (building blocks)
  * Can the candidate identify which blocks require machine learning and which do not."
* Can a person define the problem, identify relevant metrics, ideate on data sources and possible important features, understands deeply what machine learning can do.
**As machine learning is driven more by data than by algorithms**, for every formulation of the problem that you propose, you **should also tell your interviewer what kind of data and how much data you need**: both for training and for evaluating your systems.

## Reaserch vs Prod.
* In academic settings, **people care more about training** whereas **in production, people care more about serving**
* Unexpirienced candidates make the **mistake of focusing entirely on training** - like getting a model to perform well on a benchmark
* In research there is an obession with SOTA results
  * To edge out small increases in performance, researchers often make models **too complex to be useful**
  * Same goes for kaggle competitions - where ensemble of models usually wins
  * Ensembling makes your system more complex, requires much more time to develop and train, and effecitvely costs more.
  * A few percentage points might be a big deal on a leaderboard, but might not even be moticeable for users.

## Compute requirements
* Machine Learning Systems have become exponentially larger - so need more data and more compute power
* From AlexNet in 2012 to AlphaGo Zero in 2018, the compute power required increased 300k times
* These massive models make ideal headlines, not ideal products
* They are also very expensive to train and too big to fit onto costumer devices and too slow to be useful to users
> When I talk to companies that want to use machine learning in production, many tell me that they want to do what leading research labs are doing, and I have to explain to them that they don't. - *Chip Huyen*
* The goals of research are very different from goals of production.
* When asked by engineers to develop systems to be used in production, you need to keep the production goals in mind.

# Systems Design
It is an interative process with 4 components:
  1. Project setup
  2. Data pipeline
  3. Modeling (selecting, training and debugging your model)
  4. Serving (testing, deploying, maintaining)

### Project Setup
1. Goals: What do you want to achieve with this problem? - minimize the spread of misinformation, maximize revenue or users engagement
2. User Expirience: Ask your your interviewer for a step by step walkthrough of how end users are supposed to use the system.
3. Performance Constraints: How fast/good predictions have to be? What's more important: precision or recall? What's more costly: false negative or false positive? Like with cancer detection, your system must not have false negatives.
4. Evaluation: How would you evalute the perfomance of the system? During both training and inferencing?
5. Personalization: How personalized does your model have to be? Do you need one model for all the users, for a group of users or for each user individually? If you need multiple models, is it possible to train a base model on all the data and finetune it for each group or each user?
6. Project Constraints: How much time you have until deployment? How much compute power is available? What kind of talents work on the project? What available sytem be leveraged?

## Data Pipeline
> In school, you work with available, clean datasets and can spend most of your time on building and training machine learning models. In industry, you probably spend most of your time collecting, annotating, and cleaning data - *Chip Huyen*

1. Data availability and collection:
  * What kind of data is available?
  * How much data is available?
  * How much data do you already have?
  * If annotated, how good are the annotations?
  * How expensive is it to get data annotated?
  * How many annotators do you need for each sample?
  * How to resolve annotators' disagreement?
  * What's their data budget?
  * Can uttilize any of the weakly supervised or unsupervised methods to automatically create new annotated data from a small amount of humanly annotated data?
2. User data:
 * What data do you need from users?
 * How do you collect it?
 * How do you get users' feedback on the system, and if you want to use that feedback to improve the system online or periodically?
3. Storage:
 * Where is the data currently stored? On the cloud, local or on users' devices?
 * How big is each sample?
 * Does a sample fit into memory?
 * What data structures are you planning on using for the data and what are their tradeoffs?
 * How often does the new data come in?
4. Data preprocessing & representation:
 * How do you process the raw data into a form useful for your models?
 * Will you have to do any feature engineering or feature extraction?
 * Does it need noramlization?
 * What to do with missing data?
 * If there's class imbalance in the data, how do you plan on handling it?
 * How do you evaluate whether your train set and test set come from the same distribution, and what do if they don't?
 * If you have data of different types, say both text, numbers, and images, how are you planning on combining them?
5. Challanges:
 * Handling user data requires extra care, as any of the many companies that have got into trouble for user data mishandling can tell you.
6. Privacy:
 * What privacy concerns do users have about their data?
 * What anonymizing methods do you want to use on their data?
 * Can you store users' data back to your servers or can only access their data on their devices?
7. Biases:
 * What biases might represent in the data?
 * How would you correct the biases?
 * Are your data and your annotation inclusive?
 * Will your data reinforce current societal biases?

## Model Selection
> If your system has more than 100 nested if-else, it's time to switch to machine learning. - *Martin Zinkevich, a research scientist at Google*

1. You should first figure out the category of a problem - Most problems can be framed as one of the common machine learning tasks, so familiarity with common machine learning tasks and the typical approaches to solve them will be very useful
  * Is it supervised or unsupervised?
  * Is it regression or classification?
  * Does it require generation or only prediction?
  * If generation, your models will have to learn the latent space of your data, which is a much harder task than just prediction.
  * **Note that these "or" aren't mutually exclusive.** An income prediction task can be regression if we output raw numbers, but if we quantize the income into different brackets and predict the bracket, it becomes a classification problem. Similarly, you can use unsupervised learning to learn labels for your data, then use those labels for supervised learning.
  * **There are many ways to frame a problem**
2. Your goal is not to show off your knowledge of latest buzzwords, but to **use the simplest solution that can do the job**
  * Gradually adding more complex components makes it easier to debug step by step.
  * Simplest model serves as a baseline to which you can compare your more complex models.
3. Setting up an appropriate baseline is an important step that many candidates forget.
  * Random baseline: if your model just predicts everything at random, what's the expected performance?
  * Human baseline: how well would humans perform on this task?
  * Simple heuristic: for example, for the task of recommending the app to use next on your phone, **the simplest model would be to recommend your most frequently used
  app.** If this simple heuristic can predict the next app accurately 70% of the time, any model you build has to outperform it significantly to justify the added complexity
4. When considering machine learning models, don't forget that non-deep learning models exist.
  * Deep learning models are often expensive to train and hard to explain
  * They are only useful if their performance is unquestionably superior.
  * Most real world problems might not even need deep learning
  * To avoid the catch-22, you might want to launch your product without deep learning to gather user data to train your system.

## Modeling - Systematic approach

> Having a procedure for debugging and having the discipline to follow that principle are crucial in developing, implementing, and deploying machine learning models. *- Chip Huyen*

### 1. Start simple and gradually add more components

* Choose the simple architecture (e.g., LeNet on a subset of your data)
* Use sensible defaults
  * **Optimizer:** Adam Optimizer with 3e-4 (Tobin) or 3e-3 (Howard) learning rate
  * **Activations:** ReLU (FC and Conv models), tanh (LSTMs)
  * **Initialization:** He et al. normal (relu), Glorot normal (tanh)
  * **Regularization:** None
  * **Data normalization:** None
* Normalize inputs
  * Subtract mean and divide by variance
  * For images, fine to scale values to [0, 1] - (e.g., by dividing by 255) - Careful, make sure your library doesn’t do it for you!
* Simplify the problem
  * Start with a small training set (~10,000 training examples, 1000 val, 500 test)
  * Use a fixed number of objects, classes, smaller image size, etc.
  * Create a simpler synthetic training set

### 2. Implement & debug
* Start with lightweight implementation: <200 lines
* Use of the shelf components - less testing/debugging
* Start with data set you can load into memory - build complicated data pipelines later
* Overfit a single batch -try to overfit a small amount of training data and run evaluation on the same data to make sure that it gets to the smallest possible loss
* Build unit tests
* Use python debugger `ipdb` or `pdb`
* Visualize train/test losses
* Try disabling regularization
* Setting a random seed ensures consistency between different runs. It also allows you to reproduce errors and other people to reproduce your results.

3. Evaluate
  * Apply the bias-variance decomposition to decide what to do next
4. Tune hyperparameters
  * Use coarse-to-fine random searches
5. Improve model/data
  * Make your model bigger if you underfit
  * Add data or regularize if you overfit

### Dealing with multiple input modalities:
1. Map each input into a (lower-dimentional) features space
2. Flatten and concatenate feature spaceds
3. Pass through fully connected layers to output

### Top 5 DL bugs:
1. Incorrect tensor shapes (can't fail silently)
2. Preprocessing inputs incorrectly - forgetting to normalize or too much pre-processing
3. Incorrect input to your loss function - softmaxed outputs to a loss that expects logits
4. Forget to set up train mode for the net correctly - toggling train/eval - controlling batch norm dependencies
5. Numerical instability - inf/Nan - often stems from using an exp, log or div operations

### Common issues:
1. Theoretical constraints:
  * Wrong assumptions
  * Poor model selection
  * Data
2. Poor model implementation:
  * The more components a model has, the more difficult it is to figure out where is a bug
  * Moe layer moe problems
3. Snobby training techniques:
  * Calling model.train(), instead of model.eval() during evaluation
4. Poor choice of hyperparameters
  * with the same implementation, a set of hyperparameters can give you the state-of-the-art result but another set of hyperparameters might never converge.
5. Data problems:
  * mismatched inputs/labels
  * not enough data
  * class imbalances
  * noisy labels
  * train/test from different distributions

## Model - Troubleshooting:

References:
1. ML System Design by Chip Huyen
2. [Josh Tobin slides](http://josh-tobin.com/assets/pdf/troubleshooting-deep-neural-networks-01-19.pdf)
