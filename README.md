# ChatGLM2

## Overview
ChatGLM2 is a conversational model based on the Transformers library. It's trained to generate responses given a context or prompt.

## Installation
You can install the required dependencies using pip:
```
pip install transformers==4.33.2
```

## Usage
Clone the repository:
```
git clone https://github.com/rashedmamdouh/ChatGLM2.git
cd ChatGLM2
```

## Pretrained Models
This repository includes pretrained models located in the `/models` directory. You can also use your own pretrained models by specifying the path when loading the model.

## Example


```python
from transformers import AutoTokenizer, AutoModel

tokenizer = AutoTokenizer.from_pretrained("/kaggle/input/chatglm2/pytorch/6b/1")
model = AutoModel.from_pretrained("/kaggle/input/chatglm2/pytorch/6b/1").half().cuda()

response = model.chat("Hello, how are you?")
print(response)
```
