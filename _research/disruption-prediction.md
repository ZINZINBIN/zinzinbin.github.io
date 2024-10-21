---
title: "Disruption Prediction"
layout: single-portfolio
excerpt: "<img src='/images/research/disruption-prediction.png' alt=''>"
collection: research
order_number: 10
header: 
  og_image: "research/disruption-prediction.png"
---

In this research, we propose a deep learning-based approach for disruption prediction in KSTAR using In-vessel Visible Inspection System (IVIS) video and 0D parameters. Here, using video data is beneficial as it contains time-varying position and shape of plasma. We demonstrate the possibility of predicting disruption with video data only as early as approximately 20 ms before disruptions, but there is a limit over 20 ms. Thus, we incorporated 0D data and developed a multimodal model to enhance the accuracy and showed the capability of predicting disruption with multimodal data as early as 95.20 ms. To analyze model capabilities, we used t-distributed Stochastic Neighbor Embedding (t-SNE) to describe the latent space of models to compare with capabilities. We analyzed vision models using Gradient-weighted Class Activation Mapping (GradCAM) and Attention Rollout to check the abilities to capture the features. We employed permutation feature importance to identify critical 0D parameters. Consequently, we demonstrated the effectiveness of our approach for disruption prediction in KSTAR.

<iframe src="/files/Disruption-Prediction-Multimodal.pdf" width="100%" height="500" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>

## Article

Jinsu Kim. "Disruption prediction and analysis through multimodal deep learning in KSTAR" *Fusion Engineering and Design*.

[Article](https://www.sciencedirect.com/science/article/pii/S0920379624000577){: .btn--research}