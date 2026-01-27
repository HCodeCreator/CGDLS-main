# CGDLS
This is the PyTorch-based implementation for CGDLS model proposed in this paper:
![model](./framework1.png)
## Code Structures 
    .
    ├── DataHandler.py
    ├── main.py
    ├── param.py
    ├── utils.py
    ├── Utils                    
    │   ├── TimeLogger.py            
    │   ├── Utils.py                             
    ├── models
    │   ├── diffusion_process.py
    │   ├── model.py
    ├── scripts
    │   ├── run_ciao.bat
    │   ├── run_ciao.sh
    │   ├── run_epinions.bat
    │   ├── run_epinions.sh
    │   ├── run_yelp.bat
    │   ├── run_yelp.sh
    └── README

## Environment
- python=3.8
- torch=1.12.1
- numpy=1.23.1
- scipy=1.9.1
- dgl=1.1.1+cu113
- scikit-learn=1.3.2
## Datasets
Our experiments are conducted on three benchmark datasets collected from Ciao, Epinions and Yelp online platforms. In those sites, social connections can be established among users in addition to their observed implicit feedback (e.g., rating, click) over different items.

| Dataset  | # Users | # Items | # Interactions | # Social Ties |
| :------: | :-----: |:-------:|:--------------:|:-------------:|
|   Ciao   |  1,925  | 1,5053  |     23,223     |    65,084     |
| Epinions | 14,680  | 233,261 |    447,312     |    632,144    |
|   Yelp   |  99,262 | 105,142 |    672,513     |   1,298,522   |
## Evaluation Results
### Overall Performance:
CGDLS outperforms the baseline model with top-20 settings.
![performance](./result.png)

## Acknowledgements
We are particularly grateful to the authors of RecDiff, as parts of our code implementation were derived from their work. We have cited the relevant references in our paper.
Click to browse RecDiff: https://dl.acm.org/doi/abs/10.1145/3627673.3679630

## Citation
If you feel our work is insightful and want to use the code or cite our paper, please add the following citation to your paper references.
```
  @article{hu2026conditional,
  title={Conditional guided diffusion model in latent space for social recommendation},
  author={Hu, Yijun and Tang, Rui and Mo, Xian},
  journal={Applied Intelligence},
  volume={56},
  number={2},
  pages={54},
  year={2026},
  publisher={Springer}
}
```


