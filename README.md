# eMem-NDT
This is the code of our eMem-NDT to be published in ICRA2024.

Brief Introduction: In autonomous driving, predicting the behavior (turning left, stopping, etc.) of target vehicles is crucial for the self-driving vehicle to make safe decisions and avoid accidents. Existing deep learning-based methods have shown excellent and accurate performance, but the black-box nature makes it untrustworthy to apply them in practical use. In this work, we explore the interpretability of behavior prediction of target vehicles by an Episodic Memory implanted Neural Decision Tree (abbrev. eMem-NDT). The structure of eMem-NDT is constructed by hierarchically clustering the text embedding of vehicle behavior descriptions. eMem-NDT is a neural-backed part of a pre-trained deep learning model by changing the soft-max layer of the deep model to eMem-NDT, for grouping and aligning the memory prototypes of the historical vehicle behavior features in training data on a neural decision tree. Each leaf node of eMem-NDT is modeled by a neural network for aligning the behavior memory prototypes. By eMem-NDT, we infer each instance in behavior prediction of vehicles by bottom-up Memory Prototype Matching (MPM) (searching the appropriate leaf node and the links to the root node) and top- down Leaf Link Aggregation (LLA) (obtaining the probability of future behaviors of vehicles for certain instances). We validate eMem-NDT on BLVD and LOKI datasets, and the results show that our model can obtain a superior performance to other methods with clear explainability.

![image](https://github.com/JWFangit/eMem-NDT/blob/main/eMem-NDT.png)

The code link is https://github.com/YIQIONG-SPN/eMemNDT or download the whole file of "eMemNDT-main.zip".

Code Illustration:

The data loading methods are located in the "data" folder, with two files corresponding to different datasets' loading.

The main folder contains the experimental code, including NBDT, CNN_LSTM; State_former, and eMem-NDT.

All of our models are stored in the "model" folder.

The visualization of memory usage and the retrieval of the NBDT tree structure files are all saved in the "information" folder.

If your are interest this work, please cite the article as following bibtex:
