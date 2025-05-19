# cantonese-nlp-thesis: 
Cantonese Sentiment Analysis with Large Language Models

## Project Overview

This project investigates sentiment analysis in the Cantonese domain using Large Language Models (LLMs). Sentiment analysis for low-resource languages like Cantonese is challenging due to limited data and pre-trained models. This study builds a positive and negative sentiment dataset from Cantonese restaurant reviews on the OpenRice platform and applies three emoji preprocessing methods: removing emojis, retaining emojis, and converting emojis to corresponding Cantonese text.

Four Cantonese-based pre-trained large language models were trained using zero-shot and supervised fine-tuning, and their performance was compared against traditional machine learning models (Logistic Regression, SVM, Naive Bayes) and deep learning models (CNN, LSTM). The results show that fine-tuning significantly improves performance, and some Cantonese pre-trained models already demonstrate effective sentiment analysis capability. Emoji processing methods only slightly affect model performance, indicating models mainly rely on text content.

Final fine-tuned models (e.g., CantoSent-Llama3-8B-OpenRice-v1/v2/v3, CantoSent-Qwen-7B-OpenRice-v1/v2/v3) have been released on [Hugging Face](https://huggingface.co/charlottegl) to support further research and applications in Cantonese NLP.

This research can provide technical support for customer sentiment analysis in the Cantonese-speaking catering industry.

---

## Repository Structure

cantonese-nlp-thesis/
├── code/ # Code for data preprocessing, fine-tuning using LLaMA-Factory, and evaluation
├── dataset/ # Datasets
├── results/ # Evaluation metrics

---

## How to Use

### 1. Code

- All code scripts are located in the `code/` directory.
- Scripts include detailed comments and instructions.

### 2. Dataset

- Due to file size limits on GitHub, the full Cantonese restaurant review dataset is hosted externally:  
  [Download Full Dataset (Google Drive)](https://drive.google.com/drive/folders/1lk4qpUOqODdYLrO3QuU-sgPCi0ersBSl?usp=sharing))

### 3. Results

- Model evaluation metrics and comparison results can be found in the `results/` folder.

---

## Additional Resources

- Final fine-tuned Cantonese sentiment analysis models are available on Hugging Face:  
  [Hugging Face Model Repository](https://huggingface.co/charlottegl)

---

## License

This project is released under the MIT License. See the `LICENSE` file for details.

---

## Contact

For questions or collaboration, please contact:  
**Charlotte  Le Geng**  
Email: gengl@kean.edu / charlottegengl@163.com
