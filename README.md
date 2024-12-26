# Med-MAT: On the Compositional Generalization of Multimodal LLMs for Medical Imaging

## ⚡ Introduction
Welcome to the repository of Med-MAT, a VQA dataset consisting of 106 medical image-text pairs, which we hope will advance generalization experiments and aid in training powerful medical Multimodal Large Language Models (MLLMs).

Through this dataset, we have demonstrated that Compositional Generalization (CG) is one of the key mechanisms for MLLMs to understand unseen images, enabling them to handle unfamiliar images and achieve data-efficient training.

Here is a list of what has been released:

1. QA pairs for 106 collected medical datasets: These datasets consist of image-label pairs, which we transformed into VQA pairs to facilitate direct training MLLMs.
2. QA Pairs for 57 aggregated subsets: To facilitate the generalization experiments, we categorized the datasets by **M**odality, **A**natomical area, and **T**ask, then merged identical entries into subsets.
3. Image download links: Due to licensing restrictions, some datasets cannot be shared directly. Users can easily download these datasets to specified directories for use.

<div align=center>
<img src="assets/process-medmat.jpg" width = "640" alt="medmat" align=center/>
</div>


## 💭 Motivation
- To address the growing demand for quick medical consultations both online and in hospitals that do not necessarily require deep medical knowledge. We believe that LLMs like HuatuoGPT can be effectively utilized to meet these demands, freeing up physicians’ time and energy for more complex cases.
- To provide open data for training medical LLMs. Building high-quality instruction training data for LLMs is essential, but it can be also challenging. We have constructed medical instruction data using various methods and made it publicly available. This dataset can be combined with other datasets to train one's own medical 'ChatGPT'.
- To emphasize the importance of carefully evaluating the ability of medical LLMs before using them to offer medical assistance to patients. We recognize the potential benefits of LLMs in the medical field, but also acknowledge the need for thorough evaluation and testing to ensure patient safety and accurate diagnoses.

## 📚 Data

## 🤖 Limitations

Our goal with HuatuoGPT is to address the need for quick medical consultations, rather than replace doctors or provide full medical support to patients. However, our model does have several limitations that must be taken into consideration:

- Misunderstandings: As with all language models, there is a risk of misunderstandings or misinterpretations, especially when dealing with medical jargon or complex conditions. In this scenario, our models may give wrong answers.
- Hallucinations: Large language models can sometimes generate responses that do not make sense or are completely unrelated to the given input. These "hallucinations" can be especially problematic when users are not familiar with the concepts being discussed, as they may not be able to easily recognize the errors in the model's output. These "hallucinations" can be a challenge to detect and avoid.
- Bias: LLMs are trained on large datasets, which can inadvertently introduce bias into the model's responses. Additionally, care should be taken to ensure that the model is not used to perpetuate biases in medical treatment.

## Citation
```angular2
@article{huatuogpt-2023,
  title={HuatuoGPT, Towards Taming Language Models To Be a Doctor},
  author={Hongbo Zhang and Junying Chen and Feng Jiang and Fei Yu and Zhihong Chen and Jianquan Li and Guiming Chen and Xiangbo Wu and Zhiyi Zhang and Qingying Xiao and Xiang Wan and Benyou Wang and Haizhou Li},
  journal={arXiv preprint arXiv:2305.15075},
  year={2023}
}
```

We are from the Chinese University of Hong Kong, Shenzhen (CUHKSZ).
