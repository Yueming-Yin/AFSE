# AFSE
Reproducing of the paper entitled "**[AFSE: towards improving model generalization of deep graph learning of ligand bioactivities targeting GPCR proteins](https://academic.oup.com/bib/article-abstract/23/3/bbac077/6554127)**" (Briefings in Bioinformatics, 2022, IF: 13.994)

- All rights reserved by Yueming Yin, Email: 1018010514@njupt.edu.cn (or yinym96@qq.com).
- AFSE has been deployed on our web page: www.noveldelta.com/AFSE.

The [Code Ocean](https://codeocean.com) compute capsule will allow you to reproduce the results published by the author on your local machine<sup>1</sup>. Follow the instructions below, or consult [the knowledge base](https://help.codeocean.com/user-manual/sharing-and-finding-published-capsules/exporting-capsules-and-reproducing-results-on-your-local-machine) for more information. Don't hesitate to reach out via live chat or [email](mailto:support@codeocean.com) if you have any questions.

<sup>1</sup> You may need access to additional hardware and/or software licenses.

# Prerequisites

- [Docker Community Edition (CE)](https://www.docker.com/community-edition)
- [nvidia-docker](https://github.com/NVIDIA/nvidia-docker/) for code that leverages the GPU
- Licenses where applicable

# Instructions

## The computational environment (Docker image)

This capsule is private and its environment cannot be downloaded at this time. You will need to rebuild the environment locally.

> If there's any software requiring a license that needs to be run during the build stage, you'll need to make your license available. See [the knowledge base](https://help.codeocean.com/user-manual/sharing-and-finding-published-capsules/exporting-capsules-and-reproducing-results-on-your-local-machine) for more information.

In your terminal, navigate to the folder where you've extracted the capsule and execute the following command:
```shell
cd environment && docker build . --tag AFSE; cd ..
```

> This step will recreate the environment (i.e., the Docker image) locally, fetching and installing any required dependencies in the process. If any external resources have become unavailable for any reason, the environment will fail to build.

## Running the capsule to reproduce the results

In your terminal, navigate to the folder where you've extracted the capsule and execute the following command, adjusting parameters as needed:
```shell
nvidia-docker run --it \
  --workdir /AFSE \
  --volume "$PWD/data":/Benchmark_Datasets \
  --volume "$PWD/code":/AFSE \
  AFSE
```

# Reproduction on Attentive FP
## Reproducing the training process of AFSE
In your jupyter notebook, set the task ID to reproduce the training process of AFSE using the data in "Benchmark_Datasets": 
```
./AFSE/Train_AFSE.ipynb
```
## Reproducing the test and visualization process of AFSE
In your jupyter notebook, set the task ID to reproduce the training process of AFSE using the data in "Benchmark_Datasets" and the final models in "AFSE_Models":
```
./AFSE/Test&Viz_AFSE.ipynb
```
# Reproduction on other models
Please refer to "**[Molecular Property Prediction on a New CSV Dataset](https://github.com/awslabs/dgl-lifesci/tree/master/examples/property_prediction/csv_data_configuration)**"

# Citations
## In Latex
```
@article{yin2022afse,
  title={AFSE: towards improving model generalization of deep graph learning of ligand bioactivities targeting GPCR proteins},
  author={Yin, Yueming and Hu, Haifeng and Yang, Zhen and Jiang, Feihu and Huang, Yihe and Wu, Jiansheng},
  journal={Briefings in Bioinformatics},
  volume={23},
  number={3},
  pages={bbac077},
  year={2022},
  publisher={Oxford University Press}
}
```
## In Word
```
Yin, Yueming, Haifeng Hu, Zhen Yang, Feihu Jiang, Yihe Huang, and Jiansheng Wu. "AFSE: towards improving model generalization of deep graph learning of ligand bioactivities targeting GPCR proteins." Briefings in Bioinformatics 23, no. 3 (2022): bbac077.
```
