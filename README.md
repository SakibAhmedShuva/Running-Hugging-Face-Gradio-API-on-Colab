# 🚀 Running Hugging Face Gradio APIs on Google Colab

<div align="center">

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/your-notebook-link)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/SakibAhmedShuva/Running-Hugging-Face-Gradio-API-on-Colab?style=social)](https://github.com/SakibAhmedShuva/Running-Hugging-Face-Gradio-API-on-Colab)

*A comprehensive guide for programmatically using Hugging Face Spaces with Gradio APIs for image generation models like Stable Diffusion, directly within Google Colab.*

</div>

---

## 📚 Table of Contents

- [🎯 About The Project](#-about-the-project)
- [✨ Key Features](#-key-features)
- [🔧 Prerequisites](#-prerequisites)
- [🚀 Getting Started](#-getting-started)
- [📖 Notebook Breakdown](#-notebook-breakdown)
  - [Test 01: Stable Diffusion 3 (Gated Model)](#test-01-stable-diffusion-3-gated-model)
  - [Test 02: Stable Diffusion XL (Public Model)](#test-02-stable-diffusion-xl-public-model)
- [⚠️ Troubleshooting](#️-troubleshooting)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [🙏 Acknowledgments](#-acknowledgments)

---

## 🎯 About The Project

Many powerful AI models, including **Stable Diffusion 3**, are available on the Hugging Face Hub as interactive Gradio demos. While these web interfaces are excellent for manual testing, automating image generation or integrating them into workflows requires programmatic API access.

This repository provides a **single, well-documented Jupyter Notebook** (`sd.ipynb`) that demonstrates how to:

> 🔗 **Connect** to Gradio API endpoints using the `gradio_client` library  
> 🔐 **Handle authentication** for gated models requiring Hugging Face login  
> 📝 **Send prompts and parameters** to generate high-quality images  
> 🖼️ **Process and display** resulting images within the Colab environment  

This serves as a **complete template** for anyone looking to script interactions with Gradio-based Hugging Face Spaces.

---

## ✨ Key Features

<table>
<tr>
<td>

### 🌐 **Colab Ready**
Designed to run seamlessly in Google Colab with zero setup

</td>
<td>

### 🔒 **Gated Model Support**
Complete authentication workflow for restricted models

</td>
</tr>
<tr>
<td>

### 🆓 **Public Model Examples**
Quick testing with open-access models included

</td>
<td>

### 🖼️ **Advanced Image Handling**
Convert, save, and display images with professional quality

</td>
</tr>
<tr>
<td colspan="2">

### 📝 **Crystal Clear Documentation**
Every step explained with detailed comments and best practices

</td>
</tr>
</table>

---

## 🔧 Prerequisites

Before running the notebook, ensure you have:

| Requirement | Description | Action Required |
|-------------|-------------|-----------------|
| **Google Account** | For Google Colab access | [Sign up here](https://accounts.google.com/) |
| **Hugging Face Account** | Access to HF Hub and models | [Create account](https://huggingface.co/join) |
| **HF Access Token** | Token with **write permissions** | [Generate token](https://huggingface.co/settings/tokens) |
| **Model Access** | Accepted terms for gated models | [Visit SD3 model page](https://huggingface.co/stabilityai/stable-diffusion-3-medium) |

> ⚠️ **Important**: For Stable Diffusion 3, you **must** visit the model card and accept the terms of use. Skipping this step will result in access errors.

---

## 🚀 Getting Started

### Quick Start (Recommended)

1. **Click the Colab badge** at the top of this README
   
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/your-notebook-link)

2. **Run the first code cell** ("Test 01") - it will:
   - Install required libraries automatically
   - Present a Hugging Face login prompt

3. **Authenticate** when prompted:
   ```
   Please log in to Hugging Face Hub:
   Token: ········
   ```
   Paste your HF Access Token and press Enter

4. **Run remaining cells** to generate, process, and display your images

### Manual Setup

```bash
# Clone the repository
git clone https://github.com/SakibAhmedShuva/Running-Hugging-Face-Gradio-API-on-Colab.git

# Open the notebook in your preferred environment
jupyter notebook notebooks/sd.ipynb
```

---

## 📖 Notebook Breakdown

The notebook contains **two comprehensive examples** covering different use cases:

### Test 01: Stable Diffusion 3 (Gated Model)

<details>
<summary><strong>🔒 Primary Example - Full Authentication Workflow</strong></summary>

**Model**: `stabilityai/stable-diffusion-3-medium`  
**Authentication**: ✅ Required (`huggingface_hub.login()`)

**Complete Workflow**:
1. 📦 Install `gradio_client` and `Pillow`
2. 🔐 Authenticate your Hugging Face account
3. 🌐 Connect to the SD3 Gradio Space
4. 📝 Send detailed prompt and parameters to `/infer` endpoint
5. 💾 Save resulting image as permanent `.png` file
6. 🖼️ Display high-quality output in Colab

</details>

### Test 02: Stable Diffusion XL (Public Model)

<details>
<summary><strong>🆓 Secondary Example - No Authentication Required</strong></summary>

**Model**: `mojitocup/stable-diffusion-xl-base-1.0`  
**Authentication**: ❌ Not required

**Simplified Workflow**:
1. 🌐 Direct connection to SDXL Gradio Space
2. 🎨 Generate images with streamlined parameters
3. 🔄 Convert and display images instantly
4. ✅ Perfect for verifying basic setup

</details>

---

## ⚠️ Troubleshooting

<details>
<summary><strong>Common Issues & Solutions</strong></summary>

### 🚫 `RepositoryNotFoundError` or `GatedRepoError`

**Cause**: Terms of use not accepted on the model's Hugging Face page

**Solution**: 
1. Visit the [SD3 model card](https://huggingface.co/stabilityai/stable-diffusion-3-medium)
2. Log into your HF account
3. Accept the license agreement

### ⚡ `gradio_client.exceptions.AppError`

**Cause**: Hugging Face Space is busy, sleeping, or experiencing issues

**Solution**: 
- Wait 2-3 minutes and retry
- Check the Space status on Hugging Face
- Try during off-peak hours

### 🔑 Login Issues

**Cause**: Token permissions or formatting problems

**Solution**:
- Ensure token has **write permissions**
- Remove any extra spaces when copy-pasting
- Generate a new token if issues persist

</details>

---

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Ways to Contribute

- 🐛 **Report bugs** via GitHub Issues
- 💡 **Suggest features** with the "enhancement" tag
- 📖 **Improve documentation** 
- 🔧 **Submit code improvements**

### Development Workflow

```bash
# 1. Fork the repository
# 2. Create your feature branch
git checkout -b feature/AmazingFeature

# 3. Commit your changes
git commit -m 'Add some AmazingFeature'

# 4. Push to the branch
git push origin feature/AmazingFeature

# 5. Open a Pull Request
```

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License - feel free to use this project for personal and commercial purposes!
```

---

## 🙏 Acknowledgments

Special thanks to the amazing teams and individuals who made this project possible:

- 🤗 **[Hugging Face](https://huggingface.co/)** - For their incredible platform and tools
- 🎨 **[Gradio](https://gradio.app/)** - Making model interaction accessible to everyone
- 🎯 **[Stability AI](https://stability.ai/)** - For the groundbreaking Stable Diffusion 3 model
- 👨‍💻 **[mojitocup](https://huggingface.co/mojitocup)** - For the public SDXL Gradio Space

---

<div align="center">

**⭐ Found this helpful? Give us a star!**

[![GitHub stars](https://img.shields.io/github/stars/SakibAhmedShuva/Running-Hugging-Face-Gradio-API-on-Colab?style=social)](https://github.com/SakibAhmedShuva/Running-Hugging-Face-Gradio-API-on-Colab)

*Made with ❤️ by the open-source community*

</div>
