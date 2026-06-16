<h1 align="center"><b> Online Sample Average Approximation Sampling for Contrastive Decision-Focused Learning Based on Learning to Rank  </b></h1>

The following is the abstract of our paper, along with instructions for the framework and experimental procedures.

## Abstract

Decision-Focused Learning (DFL) integrates predictive modeling with downstream optimization by incorporating decision quality into the training objective. Among DFL variants, Learning to Rank (LTR) has emerged as a particularly promising approach due to its broad applicability across diverse optimization problem structures. DFL-LTR casts feasible solutions as contrastive samples and learns to predict parameters that induce rankings consistent with the true objective. However, existing DFL-LTR methods lack principled methodologies for sampling and  constructing effective ranking subsets. This fundamental gap constrains both theoretical understanding and empirical performance for contrastive learning.
To address this limitation, we propose  an online Sample Average Approximation sampling method for contrastive DFL-LTR.
 By performing stochastic optimization over minibatches, the proposed method yields an equivalent approximation of the complete solution set, suppresses loss variance to stabilise gradients, and consequently elevates the performance upper bound of the entire method.
Our LTR-SAA subset construction module is fully plug-and-play: it introduces no extra hyperparameters, incurs zero additional time complexity, and remains compatible with the entire family of LTR loss functions. In the latest open-source benchmark (comprising 7 optimization problems), our proposed method achieves SOTA decision quality on 5 of these problems. Compared with other DFL and 2-stage methods, it demonstrates significant performance advantages and generality.

##  DFL:LTR-SAA    Framework  

![example](resource/figs/idea.png)


###  Anonymity Statement
The experiments in this study are conducted based on the benchmark work by Geng et al. (NeurIPS, 2024) (cited in the main text), and their open-source source code is utilized. It should be noted that any comments and author-related information that may exist in the code belong to the original authors such as Geng et al. (NeurIPS, 2024), and are unrelated to our research team. Furthermore, we have conducted a detailed review of the used code to make every effort to ensure that no original author identity information is retained. 
   

### Install    
Prior to executing the program, decompress the archive ```code for paper.zip```  to access the core code directory ```rethink_exp.```

Prior to running this benchmark, you could install this package locally using:    
```
pip install -e .
```
### Dataset
For the dataset, we recommend using the curated "data.zip" from previous benchmark experiments. The access method is described in both the original paper and the appendix of this study. Simply place the zip file into the empty folder ```.\rethink_exp\openpto\data``` to start the experiment.


### Run of Experiment

Our experimental file is:  ```./rethink_exp/test programing.py```. After running it with a compatible Python kernel, the terminal will prompt the experimenter to select the problem and DFL method for the experiment. This selection is implemented using Python's input command. Note that you must copy the content from the printed options without any extra characters; otherwise, the program will throw an error. A specific example is as follows:

![example](resource/figs/step1.png)
![example](resource/figs/step2.png)

Subsequently, the training process will be executed automatically, with the training procedure visualized as follows:

![example](resource/figs/step3.png)

After training is completed, the system will output the final test results, which will be recorded in log.txt. The following is an example using our SOTA method on the Knapsack (Gen) problem:

![example](resource/figs/step5.png)

During the review stage, we only make some problems and methods publicly available. Your understanding is appreciated. However, it should be noted that all our SOTA methods are available for experimentation, and users can conduct experiments independently to compare results with those in the original benchmark paper.
