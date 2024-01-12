# Denoising Diffusion Probabilistic Models as a Defense against Adversarial Attacks

> Lars Ankile, Anna Midgley, Sebastian Weisshaar, Harvard University, 2022

This repository contains the code to reproduce the experiments and results in the paper. For any questions, reach out to larsankile@g.harvard.edu or open an issue in the repo. Read the final report in the [PDF located in the repo](https://arxiv.org/pdf/2301.06871.pdf).

**Abstract**

_Neural Networks are infamously sensitive to small perturbations in their inputs, making them vulnerable to adversarial attacks. This project evaluates the performance of Denoising Diffusion Probabilistic Models (DDPM) as a purification technique to defend against adversarial attacks. This works by adding noise to an adversarial example before removing it through the reverse process of the diffusion model. We evaluate the approach on the PatchCamelyon data set for histopathologic scans of lymph node sections and find an improvement of the robust accuracy by up to 88\% of the original model's accuracy, constituting a considerable improvement over the vanilla model and our baselines._

**Selected Figures**

An example of a tissue sample in the different stages of the model pipeline.

![An example of a tissue sample in the different stages of the model pipeline](Report_TeX/Figures/images_tissue.png)

The results of running our four models on 1000 test samples for both standard accuracy (left) and robust accuracy (right). The vanilla `ResNet` model is red, and our method is purple. It is also important to note that the robust adversarially trained model is an instance of a `GoogLeNet`, and not `ResNet`, as this was the only tested architecture that generalized under adversarial training.

![Model test set accuracy results](figures/comparison.pdf)

**Data**

The data used in this project is the [PatchCamelyon](https://patchcamelyon.grand-challenge.org/) data set, which is a data set of 327,680 96x96 pixel images of lymph node tissue samples. In producing our results, we created many adversarial attacks and ran them through our framework with differing purification levels. All this data is available in this ![Google Drive folder](https://drive.google.com/drive/folders/1EfnbhnjbGE-rhIuBUhB8MmLXR8wK5yGL?usp=sharing).

**Citation**

If you find this work useful, please cite it as:

```@article{ankile2023denoising,
  title={Denoising Diffusion Probabilistic Models as a Defense against Adversarial Attacks},
  author={Ankile, Lars Lien and Midgley, Anna and Weisshaar, Sebastian},
  journal={W3PHIAI workshop @ AAAI'24},
  year={2023}
}
```
