# High-Fidelity Custom Image Generation with StyleGAN2-ADA (PyTorch)

This project implements a pipeline for custom image generation and editing using generative models. The primary dataset consists of bicycle CAD designs. The goal of this project was to explore the implementation and workflow of image generation and editing rather than optimizing for final output quality or GAN metrics.


## 🚴‍♂️ Project Overview

- **Objective:** Generate and edit high-fidelity CAD-style images of bicycles.
- **Focus:** Understand the working of StyleGAN2-ADA from scratch and integrate it with powerful image editing models.
- **Dataset:** Open-source dataset of bicycle CAD designs.


## 🔧 Repositories Used

### 🎨 Image Generation Model

#### [StyleGAN2-ADA PyTorch](https://github.com/NVlabs/stylegan2-ada-pytorch)
- GAN framework used for training a custom image generation model.
- Training was done from scratch using **Google Colab Pro** compute.
- Training proceeded smoothly until around the 80th tick, where **mode collapse** was observed.
- **Note:** Model quality was considered sufficient for downstream tasks. No further fine-tuning or metric optimization was pursued as the focus was on workflow understanding.


### ✏️ Image Editing Models

#### [InstructPix2Pix](https://github.com/timothybrooks/instruct-pix2pix)
- Used to edit the GAN-generated images using **natural language prompts**.
- Inference was done using positive and negative prompts, along with a fixed seed value.
- Capably generated realistic and prompt-aligned edits.
- Delivered the best visual quality among the editing models tested.

#### [Stable Diffusion v1.5 + ControlNet](https://github.com/lllyasviel/ControlNet)
- SD1.5 used with ControlNet to provide structure-aware prompt editing.
- Results were **less consistent and less realistic** compared to InstructPix2Pix.
- Included for experimentation and comparative analysis.


## ✅ Results

- **Image Generation:** Successfully trained a model from scratch using StyleGAN2-ADA.
- **Image Editing:** InstructPix2Pix showed superior performance in prompt-guided editing.
- **ControlNet:** Included but did not outperform InstructPix2Pix in this use case.


## 🚀 Future Work

- Integrate real-time image editing through UI.
- Improve training loop to avoid mode collapse (e.g., better augmentations, restart strategies).
- Explore newer diffusion models or LoRA fine-tuning for domain-specific prompt alignment.


## 🤝 Acknowledgements

- [NVlabs/StyleGAN2-ADA-PyTorch](https://github.com/NVlabs/stylegan2-ada-pytorch)
- [Tim Brooks' InstructPix2Pix](https://github.com/timothybrooks/instruct-pix2pix)
- [ControlNet by lllyasviel](https://github.com/lllyasviel/ControlNet)

## 📬 Contact

For queries or collaboration: rlsri2305@gmail.com



