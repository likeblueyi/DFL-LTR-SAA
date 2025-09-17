<h1 align="center"><b> Decision-Focused Learning:  Learning to Rank Based on Sample Average Approximation </b></h1>

The following is the abstract of our paper, along with instructions for the framework and experimental procedures.

## Abstract

Decision-Focused Learning (DFL), also known as predict-and-optimize, improves the performance of prediction models by directly optimizing the decision quality of downstream combinatorial optimization problems. In DFL methods, learning to rank approaches demonstrate strong applicability. They treat the solution set of an optimization problem as a ranking set. Additionally, they design surrogate ranking tasks and loss functions based on the objective function.However, we observe that existing methods employ overly simplistic sampling methods for ranking subsets due to their inability to enumerate the entire solution set, neglecting the impact of such methods on the performance of learning to rank DFL methods. To address this issue, we first elaborate on the significant impact of ranking subset construction on learning to rank, including:(1) It is proven that the construction of ranking subsets affects the lower bound of the learning objective;(2) It enables the identification of an optimal subset that can equivalently replace the complete solution set, thereby clarifying the search direction  of the optimal subset. Subsequently, guided by these theoretical properties, we propose a method for constructing optimal ranking subsets based on sample sverage approximation. This improvement effectively enhances the performance of learning to rank DFL methods without compromising training efficiency. In the latest open-source benchmark (comprising 7 optimization problems), our proposed method achieves SOTA decision quality on 5 of these problems. Compared with other DFL and two-stage methods, it demonstrates significant performance advantages and generality.
The code is available in the Supplementary Material.

##  DFL:LTR-SAA    Framework  

![example](resource/figs/idea.png)




   

### Install    
Prior to running this benchmark, you could install this package locally using:    
```
pip install -e .
```
### Dataset
For the dataset, we recommend using the curated "data.zip" from previous benchmark experiments. The access method is described in both the original paper and the appendix of this study. Simply place the zip file into the empty folder ```code for paper\rethink_exp\openpto\data``` to start the experiment.

As shown in the following figure:
![example](resource/figs/data1.png)
![example](resource/figs/data2.png)
### Run of Experiment

Our experimental file is:  ```code for paper/rethink_exp/test programing.py```. After running it with a compatible Python kernel, the terminal will prompt the experimenter to select the problem and DFL method for the experiment. This selection is implemented using Python's input command. Note that you must copy the content from the printed options without any extra characters; otherwise, the program will throw an error. A specific example is as follows:
![example](resource/figs/step1.png)
![example](resource/figs/step2.png)
Subsequently, the training process will be executed automatically, with the training procedure visualized as follows:
![example](resource/figs/step3.png)

After training is completed, the system will output the final test results, which will be recorded in log.txt. The following is an example using our SOTA method on the Knapsack (Gen) problem:
![example](resource/figs/step5.png)
During the review stage, we only make some problems and methods publicly available. Your understanding is appreciated. However, it should be noted that all our SOTA methods are available for experimentation, and users can conduct experiments independently to compare results with those in the original benchmark paper.
