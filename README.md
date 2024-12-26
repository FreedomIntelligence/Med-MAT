# Med-MAT: On the Compositional Generalization of Multimodal LLMs for Medical Imaging

## ⚡ Introduction
Welcome to the repository of Med-MAT, a VQA dataset consisting of 106 medical image-text pairs, which we hope will advance generalization experiments and aid in training powerful medical Multimodal Large Language Models (MLLMs).

Through this dataset, we have demonstrated that Compositional Generalization (CG) is one of the key mechanisms for MLLMs to understand unseen images, enabling them to handle unfamiliar images and achieve data-efficient training.

Here is a list of what has been released:

1. **QA Pairs for 106 Medical Datasets**: Image-label pairs converted into VQA pairs for MLLM training.
2. **QA Pairs for 57 Aggregated Subsets**: Datasets categorized by **M**odality, **A**natomical Area, and **T**ask (MAT), with identical entries merged into subsets.
3. **Image Download Links**: Some datasets cannot be shared due to licensing. Users can download them to specified directories.

<div align=center>
<img src="assets/process-medmat.jpg" width = "800" alt="medmat" align=center/>
</div>


## 💭 QA Pairs Construction

To enable MLLMs to directly train and test on Med-MAT, the image-label pairs were converted into a Visual Question-Answering (VQA) format. The process involves the following steps:
1. **Task Definition**: Each subset was manually assigned 6 instructions to guide the MLLM in answering the task related to the subset.
2. **Conversion to VQA Format**: All image-label pairs were converted into single-choice questions with up to four answer options.
3. **Distractor Selection**: Distractor options were randomly drawn from other labels within the subset to ensure variety.
4. **Final Dataset**: The resulting dataset consisted of VQA pairs, where each image is paired with a question and four options, one of which is correct.


## 📚 Data

Original_Medical_Datasets
<details>
  <summary>Click to view the details of 106 Medical Datasets</summary>
  Hello!
</details>

Aggregated_Subsets
<details>
  <summary>Click to view the details of 57 Subsets</summary>
  Hello!
</details>

## ⚒️ How to use the data

TODO

## 🤖 Limitations

## Acknowledgement

We appreciate the previous efforts in open-sourcing the medical imaging datasets used in this project.

Please be sure to credit them when citing these datasets.

## Citation
```angular2
@article{huatuogpt-2023,
  title={HuatuoGPT, Towards Taming Language Models To Be a Doctor},
  author={Hongbo Zhang and Junying Chen and Feng Jiang and Fei Yu and Zhihong Chen and Jianquan Li and Guiming Chen and Xiangbo Wu and Zhiyi Zhang and Qingying Xiao and Xiang Wan and Benyou Wang and Haizhou Li},
  journal={arXiv preprint arXiv:2305.15075},
  year={2023}
}
```

We are from the Chinese University of Hong Kong, Shenzhen.
