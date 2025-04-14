# Forest Fire Prevention and Control Research Based on UAV Aerial Images

This repository aims to develop an open source toolkit and algorithm for early detection of forest fires using UAV aerial images and a lightweight segmentation network (FS-DeeplabV3+). Our project includes data preprocessing, model training, evaluation, as well as fire spread prediction and firebreak planning algorithms.

## Project Background

Forest fires are increasingly frequent and cause significant damage to natural resources and human life. UAVs provide a low-cost, real-time solution for monitoring forest fires. This project leverages UAV-captured images to accurately segment flames and smoke using the FS-DeeplabV3+ lightweight deep learning model, and employs geometric processing and corner detection to predict fire spread directions and plan firebreaks.

## Key Features

- **Lightweight Model**: FS-DeeplabV3+ achieves high segmentation accuracy with significantly fewer parameters, making it suitable for real-time processing on UAV platforms.
- **Fire Spread Prediction and Firebreak Planning**: Based on segmentation results, the system predicts fire spread directions using geometric analysis and corner detection algorithms, and generates optimal firebreak planning schemes.
- **Data Preprocessing and Augmentation**: Techniques such as Canny edge detection, threshold segmentation, random cropping, rotation, and flipping are applied to improve annotation accuracy and expand the dataset.

## Directory Structure

```
├── data/                  # Dataset files and data augmentation scripts
├── models/                # Model definitions, training, and inference scripts
├── utils/                 # Utility functions for preprocessing and metric calculations
├── experiments/           # Experiment configurations and result analysis
├── README.md              # This file
└── requirements.txt       # Project dependencies
```

## Installation and Usage

1. **Environment Setup**

   Clone the repository and ensure you have Python 3 installed. Then install the required dependencies with:

   ```bash
   pip install -r requirements.txt
   ```

2. **Data Preparation**

   Organize the dataset according to the guidelines in the `data/` directory. Data preprocessing and augmentation scripts are available in the `utils/` directory and can be modified as needed.

3. **Model Training and Evaluation**

   The model training, validation, and evaluation scripts are located in the `models/` directory. Start the training process by running:

   ```bash
   python models/train.py --config experiments/config.yaml
   ```

   Once training is completed, the evaluation script will output model performance metrics and generate visual results in the specified directory.

4. **Fire Spread Prediction and Firebreak Planning**

   For fire spread prediction and firebreak planning, refer to the `models/predict_fire_spread.py` script. This module processes the segmentation output to calculate fire spread directions and plan firebreaks accordingly.

## Data Sources

The data used in this project are collected from multiple public sources. The following links document the original sources and case studies:

1. [BBC Mundo - Noticias](https://www.bbc.com/mundo/noticias-62743167)
2. [Actu.fr - Faits divers](https://actu.fr/faits-divers/aveyron-un-nouveau-gros-incendie-de-vegetacion-en-cours-pres-de-millau_51821245.html)
3. [Reddit - Wildfire Discussions](https://www.reddit.com/r/Wildfire/comments/hvtquc/wildfires_rage_across_siberia_an_aerial_view/?rdt=41481)
4. [OSGeo.cn - Tech Post](https://www.osgeo.cn/post/1e956)
5. [NPS - Fire in Ecosystems: Boreal Forest](https://www.nps.gov/articles/000/fire-in-ecosystems-boreal-forest.htm)
6. [CBC News - Wildfire Containment](https://www.cbc.ca/news/canada/british-columbia/china-nose-wildfire-20-per-cent-contained-main-evacuation-order-rescinded-1.2738560)
7. [IHU Unisinos - Impact of Forest Fire Pollution on Health](https://www.ihu.unisinos.br/categorias/612623-poluicao-dos-incendios-florestais-afeta-a-saude-das-comunidades-mais-pobres)
8. [VJSHi Video Resource 1](https://www.vjshi.com/watch/13544738.html)
9. [VJSHi Video Resource 2](https://www.vjshi.com/watch/9049768.html)
10. [ChinaZ - Image Resource](https://sc.chinaz.com/tupian/160715036743.htm)
11. [VJSHi Video Resource 3](https://www.vjshi.com/watch/15463922.html)
12. [2amok - Video Text](https://www.2amok.com/videoText/436999.html)

## Contributions

Contributions are welcome! Whether you wish to optimize the code, improve the model, or integrate additional datasets, we invite your feedback and suggestions.

## License

This project is released under the [MIT License](LICENSE). You are free to use, modify, and distribute the code as long as you retain the original author information.
