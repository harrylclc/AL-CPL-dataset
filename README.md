# AL-CPL Dataset
This is the data used in "Investigating Active Learning for Concept Prerequisite Learning" (Liang et al., 2018) and "Active Learning of Strict Partial Orders: A Case Study on Concept Prerequisite Relations" (Liang et al., 2018)

### Summary
The dataset is built upon the Wiki concept map dataset by Wang et al. (2016), which is collected from textbooks on different educational domains. For each domain, the dataset consists of prerequisite pairs in the concept map. The table below summarizes the statistics of the our final processed dataset.

Domain | # Concepts | # Pairs | # Prerequisites 
 ---   | --- | --- | ---
 Data Mining | 120 | 826 | 292
 Geometry | 89 | 1681 | 524
 Physics | 153 | 1962 | 487
 Precalculus | 224 | 2060 | 699

#### Pre-processing of the Wiki concept map data (Wang et al., 2016)
In the pre-processing stage, we validate whether each of the prerequisite relations in the dataset satisfies the required properties of a strict partial order and ask domain experts to manually correct their labels if needed. We also expand the dataset by using the irreflexive and transitive properties: (i) add (B, A) as a negative sample if (A, B) is a positive sample; (ii) add (A, C) as a positive sample if both (A, B) and (B, C) are positive samples. 

### Data Description
The folder "data" contains data for the active learning experiments. All files are in the CSV format. 

- *.pairs: all concept pairs (both positive and negative examples). The task is to predict whether the second concept (2nd column) is a prerequisite of the first concept (1st column).
- *.preqs: concept pairs with prerequisite relations (positive examples). The second concept (2nd column) is a prerequisite of the first concept (1st column).

### Data Visualization
The folder "visualization" contains the data visualization of the concept prerequisite graph used in the paper. Note that only concept pairs that are in the dataset are visualized and current dataset does not include all possible concept pairs.

### Feature Files
The folder "features" includes the raw feature files used for active learning classification experiments. All files are in SVM light format.

### References
Please consider citing the following papers if you use this data.
```
@article{liang2018investigating,
  title={Investigating Active Learning for Concept Prerequisite Learning},
  author={Liang, Chen and Ye, Jianbo and Wang, Shuting and Pursel, Bart and Giles, C Lee},
  journal={Proc. EAAI},
  year={2018}
}

@article{liang2018active,
  title={Active Learning of Strict Partial Orders: A Case Study on Concept Prerequisite Relations},
  author={Liang, Chen and Ye, Jianbo and Zhao, Han and Pursel, Bart and Giles, C Lee},
  journal={arXiv preprint arXiv:1801.06481},
  year={2018}
}
```
Wiki concept map dataset
```
@inproceedings{wang2016using,
  title={Using Prerequisites to Extract Concept Maps fromTextbooks},
  author={Wang, Shuting and Ororbia, Alexander and Wu, Zhaohui and Williams, Kyle and Liang, Chen and Pursel, Bart and Giles, C Lee},
  booktitle={Proc. CIKM},
  pages={317--326},
  year={2016},
  organization={ACM}
}
```
## License
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/). 

![Alt](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)
