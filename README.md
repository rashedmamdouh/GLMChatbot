# GLMChatbot 🤖 | ChatGLM2 Conversational AI

A lightweight chatbot service built with ChatGLM2. Enables interactive language generation for English and Chinese contexts. 🧠

---

## 🧾 Overview 

GLMChatbot wraps the ChatGLM2 conversational model to generate responses in real‑time.  

---

## 🚀 Features 

- **ChatGLM2 integration:** Uses Hugging Face Transformers for generation.
- **Pretrained models included:** `/models` directory with ready-to-use weights.
- **Language support:** Handles both English and Chinese inputs with masked infilling.  
- **Light setup:** Minimal dependencies, easy to customize and extend.

---

## 🧩 Installation 

```bash
git clone https://github.com/rashedmamdouh/GLMChatbot.git
cd GLMChatbot
pip install transformers==4.33.2
````

---

## 🛠️ Usage 

Launch from a notebook or script:

```python
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM
tokenizer = AutoTokenizer.from_pretrained('path/to/model')
model = AutoModelForSeq2SeqLM.from_pretrained('path/to/model')
model.eval()

prompt = "你好 ChatGLM2!"
inputs = tokenizer(prompt, return_tensors="pt", padding=True)
outputs = model.generate(**inputs, max_length=512)
print(tokenizer.decode(outputs[0].tolist()))
```

---

## 📂 Project Structure 

```
/
├── README.md
├── glmchatbot.ipynb        # Demo notebook with usage examples
└── models/                 # Pretrained model checkpoints
```

* **glmchatbot.ipynb**: includes setup, inference, and language mixing tests
* **models/**: directory containing your downloaded pretrained weights

---

## ⚙️ Customization 

* Load your own GLM‑formatted checkpoint: specify path in code.
* Modify generation parameters: `max_length`, `num_beams`, `temperature`, etc.
* Extend to multilingual input or add `pytorch_lightning` training pipelines.


## 🧪 Future Plans 

* Add web API wrapper (FastAPI, Node.js backend with Chinese/English interface)
* Real-time UI (chat frontend) using WebSockets or React/Next.js
* Fine-tune GLM on your dataset: classification, chatbot dialogue, or domain language support

---

## 👤 Maintainer 

**Rashed Mamdouh** – AI & software engineer 👨‍💻

* Fluent in English and Arabic, studying HSK4 Chinese
* Interests: Deep Learning, Transformers, Node.js, Web‑AI integration

