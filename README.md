# Sentiment Analysis for Mental Health Monitoring in Chronic Disease Patients

This repository contains the code and results for our study on sentiment analysis of Algerian Arabic text in the context of mental health monitoring for chronic disease patients. Our work focuses on the application of transfer learning models and data augmentation techniques to address the challenges of data scarcity and imbalance in this domain.

## Abstract

Patients with chronic diseases in developing countries like Algeria face increased mental health risks and limited access to care. This study explores the use of AI, specifically sentiment analysis through transfer learning models, to aid in mental health monitoring. We conducted experiments to annotate a dataset of Algerian Arabic text and evaluated the performance of three transfer learning models: AraBERT, AraELECTRA, and DziriBERT. We also implemented various text augmentation techniques, including a novel method, to enhance model performance.

## Repository Structure

```
.
├── README.md
├── ISIA-24.ipynb
└── figures/
    ├── unfrozen/
    │   ├── Base-Arabert_PRC.png
    │   ├── Base-Arabert_ROC.png
    │   ├── AraElectra_PRC.png
    │   ├── AraElectra_ROC.png
    │   ├── DziriBert_PRC.png
    │   └── DziriBert_ROC.png
    └── frozen/
        ├── Base-Arabert_PRC.png
        ├── Base-Arabert_ROC.png
        ├── Larg-Arabert_PRC.png
        ├── Larg-Arabert_ROC.png
        ├── AraElectra_PRC.png
        ├── AraElectra_ROC.png
        ├── DziriBert_PRC.png
        └── DziriBert_ROC.png
```

## Methodology

Our study involved the following key steps:

1. Dataset collection and annotation
2. Preprocessing of Algerian Arabic text
3. Implementation of three transfer learning models: AraBERT (Base and Large), AraELECTRA, and DziriBERT
4. Application of various data augmentation techniques, including a novel method
5. Experimental evaluation with frozen and unfrozen base layers

All the code for these steps is contained in the `ISIA-24.ipynb` Jupyter notebook.

## Results

We conducted experiments comparing the performance of the transfer learning models with and without data augmentation, as well as with frozen and unfrozen base layers. Key findings include:

- Models with frozen base layers performed adequately on the positive class but poorly on the negative class.
- Unfreezing base layers led to significant improvements in performance, particularly for the negative class.
- Data augmentation techniques, especially our novel method, provided substantial improvements in model performance.
- Unfrozen models consistently outperformed frozen models, but showed a higher risk of overfitting.

### Performance Visualization

We've included Precision-Recall Curves (PRC) and Receiver Operating Characteristic (ROC) curves for each model under both frozen and unfrozen conditions. These can be found in the `figures/` directory:

- Frozen models: `figures/frozen/`
  - Base-AraBERT: `Base-Arabert_PRC.png`, `Base-Arabert_ROC.png`
  - Large-AraBERT: `Larg-Arabert_PRC.png`, `Larg-Arabert_ROC.png`
  - AraELECTRA: `AraElectra_PRC.png`, `AraElectra_ROC.png`
  - DziriBERT: `DziriBert_PRC.png`, `DziriBert_ROC.png`

- Unfrozen models: `figures/unfrozen/`
  - Base-AraBERT: `Base-Arabert_PRC.png`, `Base-Arabert_ROC.png`
  - AraELECTRA: `AraElectra_PRC.png`, `AraElectra_ROC.png`
  - DziriBERT: `DziriBert_PRC.png`, `DziriBert_ROC.png`

## Replicating the Results

To replicate the results of this study:

1. Clone this repository
2. Open the `ISIA-24.ipynb` notebook in a Jupyter environment
3. Run the notebook on Kaggle using a P100 GPU

## Conclusion

Our study provides valuable insights into the application of transfer learning and data augmentation for sentiment analysis in the context of mental health monitoring for chronic disease patients in Algeria. The results highlight the importance of carefully managing base layers in transfer learning models and the potential benefits of data augmentation techniques.

## Future Work

Future research could focus on:

1. Developing more advanced data augmentation techniques specific to Algerian Arabic
2. Exploring strategies to mitigate overfitting in unfrozen models
3. Investigating the application of these techniques in real-world mental health monitoring systems


## Contact

For any questions or concerns, please open an issue in this repository or contact the authors directly.
