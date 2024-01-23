# Machine Learning: Data Distillation, Loss, and Expert Trajectory

![image](https://github.com/EricFeng20001120/DataDistillationMHIST/assets/55144601/7ce9628c-ee3c-4167-a375-d3f5cc7c542b)

### Introduction
The world of machine learning is as fascinating as it is complex. With the explosion of data in the digital era, one of the significant challenges is processing vast datasets to extract meaningful insights. Here, we delve into the concepts of data distillation, loss minimization, and the use of expert trajectories, exploring their importance in the realm of machine learning.

### Understanding Data Distillation
Data Distillation involves transforming large, unwieldy datasets into a more manageable and potent form. This process is not just about size reduction; it's about retaining the essence of the data that's most relevant for our machine learning models.

### Why Data Distillation Matters
Efficiency: Smaller datasets mean faster processing and less computational load.
Effectiveness: Models trained on distilled data can often outperform those trained on raw, noisy datasets.

### Advancements in Data Distillation Techniques
Gradient Matching: The methodology involves a gradient comparison approach, addressing scalability issues prevalent in larger models. There will be a nested loop that tries to minimize model weights with respect to the synthetic images and minimize the synthetic images with respect to the difference in gradients.
Difficulty-Aligned Trajectory Matching (DATM): This novel approach involves aligning the difficulty of generated patterns with the size of the synthetic dataset. For larger datasets, the model minimizes loss by matching later trajectories, which capture more intricate details. Conversely, early trajectories, capturing simpler patterns, are used for smaller datasets.

### Practical Applications
The new methodology can be applied on Continual Learning, which is where new task are learned while preserving the old tasks performance. The synthetic dataset can be used in continual learning and retain more model performance than other sampling methods. It can also be applied on Neural Architecture Search, which typically requires expensive training on numerous architectures multiple times and pick the network with best validation performance, by using the condensed dataset, it will
be much faster to perform Neural Architecture Search.


### Experiments and Results: Evaluating Data Distillation Techniques
To empirically validate the efficacy of our advanced data distillation techniques, we conducted a series of experiments focusing on Gradient Matching, Temperature Tuning in Softmax, and Difficulty-Aligned Trajectory Matching (DATM).

#### Experiment Setup
Datasets: The experiments utilized the MNIST and MHIST datasets, chosen for their distinct challenges.
Models: A range of models including ConvNet, AlexNet, VGG11, and ResNet18 were used to ensure a broad evaluation.
#### Experiment Procedure and Observations
Baseline Performance: Models were initially trained on the original datasets to establish baseline performance metrics.
Synthetic Dataset Generation: Synthetic datasets were generated using our data distillation techniques, particularly focusing on Gradient Matching and DATM.
#### Evaluation on Distilled Data: Models were then trained using these synthetic datasets, and their performance was compared against the baseline models.
#### Key Results
MNIST Dataset: The test accuracy on the synthetic data was 0.91387, slightly lower than the original data's accuracy of 0.9938. This drop could be attributed to an inappropriate trajectory range during the early epochs of data distillation.
MHIST Dataset: For MHIST, the test accuracy on the synthetic data was 0.80348, surpassing the original data's accuracy of 0.7687. This indicates the efficiency of the synthetic dataset, especially in higher Information Per Class (IPC) settings.

### Conclusion
In the intricate dance of machine learning, data distillation, loss minimization, and expert trajectories play pivotal roles. Together, they create a synergy that drives forward the development of intelligent, efficient, and effective models. As we continue to push the boundaries of what's possible with AI, understanding and leveraging these concepts will be key to unlocking new and exciting advancements.

