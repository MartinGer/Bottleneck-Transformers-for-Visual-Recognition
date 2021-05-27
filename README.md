# Bottleneck-Transformers-for-Visual-Recognition
This is a pytorch implementation of the paper [Bottleneck Transformers for Visual Recognition](https://arxiv.org/abs/2101.11605 "Bottleneck Transformers for Visual Recognition") by Aravind Srinivas, Tsung-Yi Lin, Niki Parmar, Jonathon Shlens, Pieter Abbeel and Ashish Vaswani.

## Method
This paper implements the attention mechanism into different ResNet architectures. The used design of one attention layer can be displayed as shown

![botnet_layer](https://user-images.githubusercontent.com/19909320/119896434-4cf68000-bf3f-11eb-9ceb-7c6f9bb324a0.png)

Global Self-Attention on images is subject to the problem, that it can only be applied after a significant
spatial downsampling of the input. Every pixels relation is calculated to every other pixel so learning gets computationally very expensive, which prevents its usage across all layers in a fully attentional model.

Consequently in this paper the authors only apply their attention mechanism in the last stage of the respective architecture, here ResNet50:

![botnet](https://user-images.githubusercontent.com/19909320/119896460-567fe800-bf3f-11eb-815b-db71ae6b1908.png)

## Example
```python 

```
## Requirements
- pytorch
