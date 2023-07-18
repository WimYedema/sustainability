# Green Machine Learning

From https://ieeexplore.ieee.org/abstract/document/9347828:

> One of the main and yet open challenges in AutoML is an effective use of
> computational resources: An AutoML process involves the evaluation of many
> candidate pipelines, which are costly but often ineffective because they are
> canceled due to a timeout

From https://learn.microsoft.com/en-us/azure/machine-learning/concept-ml-pipelines:

> **Training efficiency and cost reduction**
> 
> Besides being the tool to put MLOps into practice, the machine learning pipeline
> also improves large model training’s efficiency and reduces cost. Taking modern
> natural language model training as an example. **It requires pre-processing
> large amounts of data and GPU intensive transformer model training. It takes
> hours to days to train a model each time.** When the model is being built, the
> data scientist wants to test different training code or hyperparameters and run
> the training many times to get the best model performance. For most of these
> trainings, there's usually small changes from one training to another one. It
> will be a significant waste if every time the full training from data processing
> to model training takes place. By using machine learning pipeline, it can
> automatically calculate which steps result is unchanged and reuse outputs from
> previous training. Additionally, the machine learning pipeline supports running
> each step on different computation resources. Such that, the memory heavy data
> processing work and run-on high memory CPU machines, and the computation
> intensive training can run on expensive GPU machines. By properly choosing which
> step to run on which type of machines, the training cost can be significantly
> reduced.