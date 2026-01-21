
---

# Indic Transliteration Model (Indic → Roman)

This project trains and deploys an **Indic-to-English (Roman) transliteration model** for multiple Indian languages (Hindi, Bengali, Tamil) using:

* **Aksharantar dataset**
* **mT5 (Multilingual T5)**
* **CTranslate2** for optimized inference
* **Gradio** for a web-based demo

The entire pipeline is designed to run step-by-step in **Google Colab** with GPU support.

---

## Project Pipeline

The notebook follows a clear 6-step workflow:

1. **Install dependencies**
2. **Load & preprocess dataset**
3. **Train mT5 transliteration model**
4. **Evaluate model performance**
5. **Optimize model with CTranslate2**
6. **Launch Gradio demo**

---

## Supported Languages

* Hindi
* Bengali
* Tamil

(Input: native script → Output: Romanized text)

---

## Requirements

The notebook installs all dependencies automatically, but the main libraries used are:

* `datasets`
* `transformers`
* `torch`
* `accelerate`
* `sentencepiece`
* `ctranslate2`
* `gradio`
* `huggingface_hub`
* `sacrebleu`

GPU is **strongly recommended** for training.

---

## How to Run

### 1. Open in Google Colab

Upload `model_training_indic.ipynb` to Colab and enable GPU:

```
Runtime → Change runtime type → GPU
```

### 2. Run Cells Sequentially

Execute each step in order:

* **Step 1**: Install dependencies
* **Step 2**: Load and preprocess Aksharantar dataset
* **Step 3**: Train the mT5 model
* **Step 4**: Evaluate transliteration quality
* **Step 5**: Convert model to CTranslate2 for faster inference
* **Step 6**: Launch Gradio demo

---

## Model Output

* Trained model is saved to:

  ```
  ./translit-model
  ```
* Optimized CTranslate2 model is generated with reduced size and faster inference.

---

## Gradio Demo

The final step launches an interactive Gradio UI where you can:

* Select a language
* Enter Indic text
* Get Romanized transliteration instantly

This makes the model easy to test and showcase.

---

## Use Cases

* Search normalization
* Speech & NLP preprocessing
* Indic language input methods
* Romanized text generation

---

## Notes

* The project is optimized for **clarity and speed**, not massive-scale training.
* Ideal for research, demos, and rapid prototyping.
* Dataset size and training steps can be adjusted easily in the notebook.

---

## License

Specify your license here (e.g., MIT, Apache 2.0).

---
