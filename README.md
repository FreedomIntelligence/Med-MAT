# Med-MAT: On the Compositional Generalization of Multimodal LLMs for Medical Imaging

## ⚡ Introduction
Welcome to the repository of Med-MAT, a VQA dataset consisting of 106 medical image-text pairs, which we hope will advance generalization experiments and aid in training powerful medical multimodal large language models (MLLMs).

Through this dataset, we have demonstrated that Compositional Generalization (CG) is one of the key mechanisms for MLLMs to understand unseen images, enabling them to handle unfamiliar images and achieve data-efficient training.

<div align=center>
<img src="assets/process-medmat.jpg" width = "800" alt="medmat" align=center/>
</div>

Here is a list of what has been released:

1. **QA Pairs for 106 Medical Datasets**: Image-label pairs converted into VQA pairs for MLLM training.
2. **QA Pairs for 53 Aggregated Subsets**: Datasets categorized by **M**odality, **A**natomical Area, and **T**ask (MAT), with identical entries merged into subsets.
3. **Image Download Links**: Some datasets cannot be shared due to licensing. Users can download them to specified directories.


## 💭 QA Pairs Construction

To enable MLLMs to directly train and test on Med-MAT, the image-label pairs were converted into a Visual Question-Answering (VQA) format. The process involves the following steps:
1. **Task Definition**: Each subset was manually assigned 6 instructions to guide the MLLM in answering the task related to the subset.
2. **Conversion to VQA Format**: All image-label pairs were converted into single-choice questions with up to four answer options.
3. **Distractor Selection**: Distractor options were randomly drawn from other labels within the subset to ensure variety.
4. **Final Dataset**: The resulting dataset consisted of VQA pairs, where each image is paired with a question and four options, one of which is correct.


## 📚 Data

You can access the QA pairs of Med-MAT through [HF Link](https://huggingface.co/datasets/FreedomIntelligence/Med-MAT).

The table below provides the download links for all datasets. After downloading the images to the "med-mat" folder and placing the corresponding JSON files as shown, you can easily access Med-MAT.

```
┬─ med-mat
│   ├─ CT_Kindney_Dataset
│   └─ ... (unzipped datasets)
└─ Aggregated_Subsets
│   ├─ Subset--01-train.json
│   ├─ Subset--02-train.json
│   └─ ... (other subsets)
└─ Original_Medical_Datasets
    ├─ Ori--01-train.json
    ├─ Ori--02-train.json
    └─ ... (other medical datasets)
```

If you only want to use some part of the Med-MAT datasets, you can selectively download the corresponding images and JSON files for the chosen datasets.

**Original_Medical_Datasets**
<details>
<summary>Click to view the details of 106 Medical Datasets</summary>

| **No.** | **Name with link** | **Modality** | **Area** | **Task** |
| ------ | ------- | ------- | -------- | -------- |
| 1 |[Intel and MobileODT Cervical Screening](https://www.kaggle.com/competitions/intel-mobileodt-cervical-cancer-screening/data)|Co|Cervix|Cervix Type in Screening|
| 2 |[CT Kindney Dataset](https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone)|CT|Kidney|Normal or Cyst or Tumor|
| 3 |[SARS-COV-2 Ct-Scan](https://www.kaggle.com/datasets/plameneduardo/sarscov2-ctscan-dataset)|CT|Lung|COVID19, Classification Dataset|
| 4 |[COVID CT COVID-CT](https://tianchi.aliyun.com/dataset/106604)|CT|Lung|COVID19, Classification Dataset.|
| 5 |[Chest CT-Scan](https://tianchi.aliyun.com/dataset/93929)|CT|Lung|Cancer, 3 Cancer Categories, Multiple Classification Dataset|
| 6 |[COVID-19-CT SCAN IMAGES](https://tianchi.aliyun.com/dataset/93666)|CT|Lung|COVID19, Classification|
| 7 |[Head CT](https://www.kaggle.com/datasets/felipekitamura/head-ct-hemorrhage?select=labels.csv)|CT|Brain|Head Hemorrhage|
| 8 |[CT of Brain](https://www.kaggle.com/datasets/trainingdatapro/computed-tomography-ct-of-the-brain)|CT|Brain|Head Cancer|
| 9 |[MED-NODE](https://www.cs.rug.nl/~imaging/databases/melanoma_naevi/)|Der|Skin|Melanoma or Naevus|
| 10 |[ISIC 2020](https://challenge2020.isic-archive.com/)|Der|Skin|Melanoma, Benign or Malignant|
| 11 |[PED-UFES-20](https://data.mendeley.com/datasets/zr7vgbcyr2/1)|Der|Skin|Skin Multi Classification|
| 12 |[Web-scraped Skin Image](https://www.kaggle.com/datasets/arafathussain/monkeypox-skin-image-dataset-2022)|Der|Skin|Skin Desease Multi Classification|
| 13 |[ISBI 2016](https://www.kaggle.com/datasets/angelachristabel/isbi-2016?select=Training_GroundTruth.csv)|Der|Skin|Skin Lesion Classification|
| 14 |[ISIC 2019](https://www.kaggle.com/datasets/andrewmvd/isic-2019)|Der|Skin|Skin Desease Multi Classification|
| 15 |[Skin Cancer ISIC](https://www.kaggle.com/datasets/nodoubttome/skin-cancer9-classesisic)|Der|Skin|Skin Cancer Multi Classification|
| 16 |[Dental Condition Dataset](https://www.kaggle.com/datasets/salmansajid05/oral-diseases/data)|DP|Teeth|Teeth condition classification|
| 17 |[Oral Cancer Dataset](https://www.kaggle.com/datasets/zaidpy/oral-cancer-dataset)|DP|Teeth|Oral cancer Classification|
| 18 |[The Nerthus Dataset](https://datasets.simula.no/nerthus/)|End|Intestine|Cleanliness level|
| 19 |[Endoscopic Bladder Tissue](https://commons.datacite.org/doi.org/10.5281/zenodo.7741475)|End|Bladder|Canser Degree Classification|
| 20 |[Kvasir](https://www.kaggle.com/datasets/meetnagadia/kvasir-dataset)|End|Intestine|Multi Disease Classification|
| 21 |[ACRIMA](https://figshare.com/s/c2d31f850af14c5b5232)|FP|Fundus|Glaucoma|
| 22 |[Augemnted ocular diseases AOD](https://www.kaggle.com/datasets/nurmukhammed7/augemnted-ocular-diseases)|FP|Fundus|Multi Classification of eye diseases|
| 23 |[JSIEC](https://www.kaggle.com/datasets/linchundan/fundusimage1000)|FP|Fundus|Multi Classification of eye diseases|
| 24 |[Multi-Label Retinal Diseases](https://data.mendeley.com/datasets/pc4mb3h8hz/1)|FP|Fundus|Multi Classification of eye diseases|
| 25 |[RFMiD 2.0](https://github.com/openmedlab/Awesome-Medical-Dataset/blob/main/resources/RFMiD.md)|FP|Fundus|Multi Classification of eye diseases|
| 26 |[ToxoFundus(Data Processed Paper)](https://www.kaggle.com/datasets/nafin59/ocular-toxoplasmosis-fundus-images-dataset)|FP|Fundus|Ocular toxoplasmosis|
| 27 |[ToxoFundus(Data Raw 6class All)](https://www.kaggle.com/datasets/nafin59/ocular-toxoplasmosis-fundus-images-dataset)|FP|Fundus|Ocular toxoplasmosis|
| 28 |[Adam dataset](https://www.kaggle.com/datasets/xiaoliang2121/adamdataset)|FP|Fundus|Age-related Macular Degeneration|
| 29 |[APTOS 2019 Blindness](https://www.kaggle.com/competitions/aptos2019-blindness-detection)|FP|Fundus|Blindness Level Identification 0~4|
| 30 |[DRIMBD](https://www.kaggle.com/datasets/subhajournal/drimdb-diabetic-retinopathy-images-database)|FP|Fundus|Quality Testing of Retinal Images|
| 31 |[Glaucoma Detection](https://www.kaggle.com/datasets/sshikamaru/glaucoma-detection)|FP|Fundus|Glaucoma Classification|
| 32 |[AIROGS](https://zenodo.org/records/93241)|FP|Fundus|Glaucoma Classification|
| 33 |[ICPR-HEp-2](https://github.com/KaikaiZhao/HEp-2_cell_classification)|Mic|Cell|Multi Classification|
| 34 |[SICAPv2](https://data.mendeley.com/datasets/9xxm58dvs3/1)|Mic|Cell|Cancer Degree Classification|
| 35 |[Blood Cell Images](https://www.kaggle.com/datasets/paultimothymooney/blood-cells)|Mic|Cell|Blood Cell Classificaion (Multi)|
| 36 |[BreakHis](https://www.kaggle.com/datasets/ambarish/breakhis)|Mic|Cell|Cell type and beginormag|
| 37 |[Chaoyang](https://bupt-ai-cz.github.io/HSA-NRL/)|Mic|Cell|Multi Classification of pathologists|
| 38 |[HuSHeM](https://data.mendeley.com/datasets/tt3yj2pf38/3)|Mic|Cell|Sperm Head Morphology Classificaion|
| 39 |[Bone Marrow Cell Classification](https://www.kaggle.com/datasets/andrewmvd/bone-marrow-cell-classification)|Mic|Cell|Bone Marrow Cell Classification|
| 40 |[NCT-CRC-HE-100K](https://zenodo.org/records/1214456)|Mic|Cell|Multi Classification|
| 41 |[Malignant Lymphoma Classification](https://www.kaggle.com/datasets/andrewmvd/malignant-lymphoma-classification)|Mic|Cell|Multi Classification|
| 42 |[Histopathologic Cancer Detection](https://www.kaggle.com/c/histopathologic-cancer-detection/data)|Mic|Cell|Cancer Classification|
| 43 |[LC25000](https://www.kaggle.com/datasets/xilezhu/lc25000)|Mic|Cell|Multi Classification of Lung and Colon|
| 44 |[Brain Tumor 17 Classes](https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-17-classes)|MRI|Brain|Multi Classification|
| 45 |[Tumor Classification](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)|MRI|Brain|Pituitary or Glioma or Meningioma or Notumor|
| 46 |[Malignant Lymphoma Classification](https://www.kaggle.com/datasets/andrewmvd/malignant-lymphoma-classification)|OCT|Retina|Multi Classification of eye diseases|
| 47 |[Retinal OCT-C8](https://www.kaggle.com/datasets/obulisainaren/retinal-oct-c8)|OCT|Retina|Multi Classification of eye diseases|
| 48 |[BUSI](https://www.kaggle.com/datasets/sabahesaraki/breast-ultrasound-images-dataset)|US|Breast|Breast Cancer|
| 49 |[Digital Knee X-Ray Images](https://data.mendeley.com/datasets/t9ndx37v5h/1)|X-Ray|Bones|Degree Classification of Knee|
| 50 |[Bone Fracture Multi-Region X-ray Data](https://www.kaggle.com/datasets/preetviradiya/brian-tumor-dataset)|X-Ray|Bones|Fractured Classification|
| 51 |[Fracture detection](https://www.kaggle.com/datasets/devbatrax/fracture-detection-using-x-ray-images)|X-Ray|Bones|Fractured Classification|
| 52 |[The vertebrae X-ray image](https://www.kaggle.com/datasets/yasserhessein/the-vertebrae-xray-images)|X-Ray|Bones|Vertebrae|
| 53 |[Knee Osteoarthritis Dataset](https://www.kaggle.com/datasets/shashwatwork/knee-osteoarthritis-dataset-with-severity)|X-Ray|Bones|Knee Osteoarthritis with severity grading|
| 54 |[Shenzhen Chest X-Ray Set](https://lhncbc.nlm.nih.gov/LHC-downloads/downloads.html#tuberculosis-image-data-sets)|X-Ray|Lung|COVID19, Classification Dataset.|
| 55 |[Chest X-ray PD](https://data.mendeley.com/datasets/jctsfj2sfn/1)|X-Ray|Lung|COVID and Pneumonia|
| 56 |[COVID-19 CHEST X-RAY DATABASE](https://www.heywhale.com/mw/dataset/6027caee891f960015c863d7/content)|X-Ray|Lung|COVID and Pneumonia|
|  |[COVIDGR](https://github.com/ari-dasci/covidgr)|X-Ray|Lung|COVID19, Classification|
| 58 |[MIAS](https://www.kaggle.com/datasets/kmader/mias-mammography)|X-Ray|Breast|Multi Classification of Breast|
| 59 |[Tuberculosis Chest X-Ray Database](https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset)|X-Ray|Lung|Tuberculosis|
| 60 |[Pediatric Pneumonia Chest X-Ray](https://www.kaggle.com/datasets/andrewmvd/pediatric-pneumonia-chest-xray)|X-Ray|Lung|Pneumonia Classification|
| 61 |[Random Sample of NIH Chest X-Ray Dataset](https://www.kaggle.com/datasets/nih-chest-xrays/sample)|X-Ray|Chest|Multi Classificaiton of Chest|
| 62 |[CoronaHack-Chest X-Ray](https://www.kaggle.com/datasets/praveengovi/coronahack-chest-xraydataset)|X-Ray|Lung|Pnemonia Classifcition with Virus type|
| 63 |[Brain Tumor Dataset](https://www.kaggle.com/datasets/preetviradiya/brian-tumor-dataset)|X-Ray|Brain|Tumor Classification|
| 64 |[Fitzpatrick 17k (Nine Labels)](https://github.com/mattgroh/fitzpatrick17k)|Der|Skin|Multi Classification|
| 65 |[BioMediTech](https://figshare.com/s/d6fb591f1beb4f8efa6f)|Mic|Cell|Multi Classification|
| 66 |[Diabetic retinopathy](https://zenodo.org/records/4891308)|FP|Fundus|Diabetic Retinopathy Level|
| 67 |[Leukemia](https://tianchi.aliyun.com/dataset/90101/notebook)|Mic|Cell|Cancer Classification|
| 68 |[ODIR-5K](https://odir2019.grand-challenge.org/introduction/)|FP|Fundus|Multiple Labels Classification|
| 69 |[Arthrosis](https://aistudio.baidu.com/datasetdetail/69582/0)|X-Ray|Bones|Bone Age Classification|
| 70 |[HSA-NRL](https://bupt-ai-cz.github.io/HSA-NRL/)|Mic|Cell|Multi Classification of pathologists|
| 71 |[ISIC 2018 (Task 3)](https://challenge.isic-archive.com/data/#2018)|Der|Skin|Multi Classification|
| 72 |[ISIC 2017 (Task 3)](https://challenge.isic-archive.com/data/#2018)|Der|Skin|Multi Classification|
| 73 |[ChestX-Det](https://opendatalab.com/OpenDataLab/ChestX-Det)|X-Ray|Chest|Multi Classification|
| 74 |[Monkeypox Skin Lesion Dataset](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset)|Der|Skin|Only Monkeypox|
| 75 |[Cataract Dataset](https://www.kaggle.com/datasets/jr2ngb/cataractdataset)|FP|Fundus|Multi Classification|
| 76 |[ChestX-rays IndianaUniversity](https://www.kaggle.com/datasets/raddar/chest-xrays-indiana-university?select=indiana_reports.csv)|X-Ray|Chest|Multi-label Classification|
| 77 |[CheXpert v1.0 small](https://www.kaggle.com/datasets/willarevalo/chexpert-v10-small)|X-Ray|Chest|Multi-label Classification|
| 78 |[CBIS-DDSM](https://www.kaggle.com/datasets/awsaf49/cbis-ddsm-breast-cancer-image-dataset)|X-Ray|Breast|Multi Classification|
| 79 |[NLM-TB](https://www.kaggle.com/datasets/nurkaraca/nlm-montgomerycxrset)|X-Ray|Lung|Tuberculosis|
| 80 |[ChestXray-NIHCC](https://nihcc.app.box.com/v/ChestXray-NIHCC/folder/36938765345)|X-Ray|Chest|Multi-label Classification|
| 81 |[COVIDx CXR-4](https://www.kaggle.com/datasets/andyczhao/covidx-cxr2)|X-Ray|Lung|COVID19, Classification|
| 82 |[VinDr-Mammo](https://www.kaggle.com/datasets/ssmann/vindr-mammo-dataset)|X-Ray|Breast|Multi-label Classification|
| 83 |[PBC dataset normal DIB](https://data.mendeley.com/datasets/snkd93bnjr/1)|Mic|Cell|Multi Classification|
| 84 |[Human Protein Atlas](https://www.kaggle.com/competitions/hpa-single-cell-image-classification/data?select=train.csv)|Mic|Cell|Multi-label Classification (Only green)|
| 85 |[RSNA Pneumonia Detection Challenge 2018](https://www.rsna.org/rsnai/ai-image-challenge/rsna-pneumonia-detection-challenge-2018)|X-Ray|Chest|Multi-label Classification|
| 86 |[VinDr-SpineXR](https://www.physionet.org/content/vindr-spinexr/1.0.0/)|X-Ray|Bones|Multi Classification of Bones Diseases|
| 87 |[VinDr-PCXR](https://physionet.org/content/vindr-pcxr/1.0.0/)|X-Ray|Chest|Multi-label Classification|
| 88 |[PH2](https://paperswithcode.com/dataset/ph2)|Der|Skin|Melanoma Segmentation|
| 89 |[ISBI 2016 (Task3B)](https://www.kaggle.com/datasets/angelachristabel/isbi-2016?select=Training_GroundTruth.csv)|Der|Skin|Melanoma Segmentation|
| 90 |[ISIC 2016 (Task 1)](https://challenge.isic-archive.com/data/#2018)|Der|Skin|Melanoma Segmentation|
| 91 |[ISIC 2017](https://challenge.isic-archive.com/data/#2018)|Der|Skin|Melanoma Segmentation|
| 92 |[CVC-ClinicDB](https://polyp.grand-challenge.org/CVCClinicDB/)|End|Intestine|Polyp Segmentation|
| 93 |[Kvasir-SEG](https://datasets.simula.no/kvasir-seg/)|End|Intestine|Polyp segmentation|
| 94 |[m2caiseg](https://www.kaggle.com/datasets/salmanmaq/m2caiseg)|End|Intestine|Surgical Instrument Segmentation|
| 95 |[EDD 2020](https://edd2020.grand-challenge.org/Data/)|End|Intestine|Multiple Diseases Segmentation in Intestine|
| 96 |[SICAPv2](https://data.mendeley.com/datasets/9xxm58dvs3/1)|Mic|Cell|Cancer Cells Segmentation|
| 97 |[BUSI](https://www.kaggle.com/datasets/sabahesaraki/breast-ultrasound-images-dataset)|Ultrasound|Breast|Cancer Segmentation|
| 98 |[TN3K](https://github.com/haifangong/TRFE-Net-for-thyroid-nodule-segmentation)|Ultrasound|Thyroid|Thyroid Nodule Segmentation|
| 99 |[NLM-TB](https://openi.nlm.nih.gov/imgs/collections/NLM-MontgomeryCXRSet.zip)|X-Ray|Lung|Lung Segmentation (With left or right)|
| 100 |[VinDr-SpineXR](https://www.physionet.org/content/vindr-spinexr/1.0.0/)|X-Ray|Bones|Spinal X-ray Anaomaly Detection|
| 101 |[VinDr-PCXR](https://physionet.org/content/vindr-pcxr/1.0.0/)|X-Ray|Chest|Multiple Diseases Segmentation in Chest|
| 102 |[ChestX-Det](https://opendatalab.com/OpenDataLab/ChestX-Det)|X-Ray|Chest|Multiple Diseases Segmentation in Chest|
| 103 |[UW-Madison Gl Tract Image Segmentation](https://www.kaggle.com/competitions/uw-madison-gi-tract-image-segmentation/overview)|MRI|Intestine|Surgical Instrument Segmentation|
| 104 |[Duke Liver Dataset MRI v1](https://zenodo.org/records/7774566)|MRI|Liver|Liver Segmentation|
| 105 |[Duke Liver Dataset MRI v2](https://zenodo.org/records/7774566)|MRI|Liver|Liver Segmentation|
| 106 |[SIIM-ACR Pneumothorax Segmentation](https://www.kaggle.com/c/siim-acr-pneumothorax-segmentation)|X-Ray|Lung|Pneumothorax Segmentation|
| 107 |[FIVES](https://figshare.com/articles/figure/FIVES_A_Fundus_Image_Dataset_for_AI-based_Vessel_Segmentation/19688169/1?file=34969398)|FP|Fundus|Fundus Vascular Segmentation|
| 108 |[RIM-ONE DL](https://github.com/miag-ull/rim-one-dl?tab=readme-ov-file)|FP|Fundus|Optic Disc and Cup Segmentation|
| 109 |[PALM19](https://ieee-dataport.org/documents/palm-pathologic-myopia-challenge)|FP|Fundus|Optic Disc Segmentation|
  
</details>

**Aggregated_Subsets**
<details>
  <summary>Click to view the details of 53 Subsets</summary>

| **No.**| **Modality** | **Area** | **Task** |
| ------ | ------- | -------- | -------- |
|01 | Co | Cervix | Cervical Picture Quality Evaluation |
|02 | CT | Kidney | Kidney Diseases Classification |
|03 | CT | Lung | COVID-19 Classification |
|04 | CT | Lung | Lung Cancer Classification |
|05 | CT | Brain | Brain Hemorrhage Classification |
|06 | CT | Brain | Brain Cancer Classification |
|07 | Der | Skin | Melanoma Type Classification |
|08 | Der | Skin | Skin Diseases Classification |
|09 | DP | Mouth | Teeth Condition Classification |
|10 | DP | Mouth | Oral Cancer Classification |
|11 | End | Intestine | Intestine Cleanliness Level |
|12 | End | Bladder | Cancer Degree Classification |
|13 | End | Intestine | Intestine Diseases Classification |
|14 | FP | Fundus | Eye Diseases Classification |
|15 | FP | Fundus | Multiple-labels Eye Diseases Classification |
|16 | FP | Fundus | Blindness Level |
|17 | FP | Fundus | Retinal Images Quality Evaluation |
|18 | Mic | Cell | Cell Type Classification |
|19 | Mic | Cell | Prostate Cancer Degree Classification |
|20 | Mic | Cell | Multiple-labels Blood Cell Classification |
|21 | Mic | Cell | Cancer Classification |
|22 | MRI | Brain | Head Diseases Classification |
|23 | OCT | Retina | Retina Diseases Classification |
|24 | US | Breast | Breast Cancer Classification |
|25 | X-ray | Bones | Degree Classification of Knee |
|26 | X-ray | Bones | Fractured Classification |
|27 | X-ray | Bones | Vertebrae Diseases Classification |
|28 | X-ray | Lung | COVID-19 and Pneumonia Classification |
|29 | X-ray | Breast | Breast Diseases Classification |
|30 | X-ray | Lung | Tuberculosis Classification |
|31 | X-ray | Chest | Multiple-labels Chest Classification |
|32 | X-ray | Brain | Tumor Classification |
|33 | Mic | Cell | Multi-labels Diseases |
|34 | FP | Fundus | Level Identification |
|35 | X-ray | Bones | Level Identification |
|36 | X-ray | Bones | Spinal lesion Classification |
|37 | X-ray | Breast | Multi-labels Diseases |
|38 | Der | Skin | Lesion Det/Seg |
|39 | End | Intestine | PolyP Det/Seg |
|40 | End | Intestine | Surgical Procedures Det/Seg |
|41 | End | Intestine | Multi-labels Det/Seg |
|42 | Mic | Cell | Cancer Cell Det/Seg |
|43 | US | Chest | Cancer Det/Seg |
|44 | US | Thyroid | Thyroid Nodule Region Det/Seg |
|45 | MRI | Intestine | Multi-labels Det/Seg |
|46 | MRI | Liver | Liver Det/Seg |
|47 | X-ray | Lung | Lung Det/Seg |
|48 | X-ray | Lung | Pneumothorax Det/Seg |
|49 | X-ray | Bones | Spinal Anomaly Det |
|50 | X-ray | Chest | Multi-labels Det |
|51 | FP | Fundus | Vessel Seg |
|52 | FP | Fundus | Optic Disc and Cup Seg |
|53 | FP | Fundus | Optic Disc Seg |
</details>

## ⚒️ Data Construction

Here’s a sample from Med-MAT:
- **caption**: The original label from the collected medical datasets.
- **image**: Path to the corresponding image.
- **Question** and **Answer**: Caption-based QA pairs.
- **Question-choice** and **Answer-choice**: Multiple-choice QA pairs.
- **data-no**: Number of its original medical dataset.
```json
{
    "id": 1,
    "caption": "Cyst",
    "image": "med-mat/CT_Kindney_Dataset/CT-KIDNEY-DATASET-Normal-Cyst-Tumor-Stone/CT-KIDNEY-DATASET-Normal-Cyst-Tumor-Stone/Cyst/Cyst- (561).jpg",
    "Question": "Review this kidney CT scan and determine the possible condition it represents.",
    "Answer": "Cyst",
    "Question-choice": "Review this kidney CT scan and determine the possible condition it represents.\nA: Stone\nB: Cyst\nC: Normal\nD: Tumor\nAnswer with the option's letter from the given choices directly.",
    "Answer-choice": "B",
    "data-no": "2"
}
```

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
