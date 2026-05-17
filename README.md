# Bol-AI v1.0

<p align="center">
  <img src="https://i.ibb.co/s9X3yR1f/In-Shot-20260117-214933669.jpg" width="230" alt="Bol-AI Logo"/>
</p>

<h1 align="center">Bol-AI</h1>
<h3 align="center">A Custom, Lightweight Conversational AI Assistant</h3>
<p align="center">Developed & Engineered by Vivek Vijay Dalvi • MAHAVEER AI</p>

---

## 📌 About Bol-AI

Bol-AI is a custom conversational AI assistant developed and fine-tuned by Vivek Vijay Dalvi under **MAHAVEER AI**. This project focuses on delivering a highly optimized, lightweight, and intelligent conversational experience that can run on standard hardware, including mobile devices.

The model has been engineered with a custom identity, enhanced with multilingual datasets (English, Marathi, Hindi), and fine-tuned for superior instruction-following and coding assistance.

- **Official Documentation:** [bol-ai-docs.web.app](https://bol-ai-docs.web.app)

---

## ✨ Core Features

- **Intelligent Conversational Responses:** Human-like, context-aware replies.
- **Custom AI Personality System:** Unique identity and behavior engineered by Vivek Dalvi.
- **Multilingual Understanding:** Natively supports English, Marathi, and Hindi.
- **Expert Coding Assistance:** Optimized for instruction-following in various programming languages.
- **Ultra-Lightweight & Fast:** At just 2.5 GB, it is designed for efficient local deployment on standard hardware.
- **Privacy-Focused:** Runs 100% offline, ensuring user data remains secure.
- **Mobile Ready:** Optimized to run on high-end mobile devices with sufficient RAM.

---

## 🧠 Full Model Information

| Property                  | Details                                                                 |
|---------------------------|-------------------------------------------------------------------------|
| **Model Name**            | Bol-AI                                                                  |
| **AI Category**           | Conversational AI Assistant                                             |
| **Developer**             | Vivek Vijay Dalvi                                                       |
| **Organization**          | MAHAVEER AI                                                             |
| **Base Model**            | MiniCPM-V-4.6 (Heavily Fine-Tuned)                                      |
| **Base Model Developer**  | OpenBMB                                                                 |
| **Architecture**          | Transformer                                                             |
| **Parameter Count**       | ~1.7 Billion                                                            |
| **Context Length**        | 32,000 Tokens                                                           |
| **Model Size**            | 2.42 GB                                                                 |
| **Quantization**          | 4-bit Optimized (NF4)                                                   |
| **Model Format**          | SafeTensors                                                             |
| **Primary Language**      | English                                                                 |
| **Supported Languages**   | English, Marathi, Hindi                                                 |
| **License**               | Apache-2.0                                                              |

---

## 🛠️ Training & Customization

Bol-AI's superior performance is the result of extensive fine-tuning and engineering, including:

- **Conversational Fine-Tuning:** Trained on over 65,000 high-quality instruction rows.
- **Identity Engineering:** Deeply baked identity ensures the model recognizes its creator and purpose.
- **Response Optimization:** Tuned for accuracy, relevance, and consistency.
- **Multilingual Data Integration:** Enhanced with custom datasets for Indian languages.
- **Behavioral Tuning:** Personality and interaction style refined for a professional assistant experience.

---

## 💻 System Requirements

Bol-AI is highly optimized to run on a wide range of devices.

### Desktop / Laptop

| Component         | Minimum (CPU-Only)                        | Recommended (GPU for Speed)               |
|-------------------|-------------------------------------------|-------------------------------------------|
| **System RAM**    | 8GB                                       | 16GB+                                     |
| **GPU VRAM**      | Not Required                              | 4GB+ (NVIDIA CUDA Recommended)            |
| **Storage**       | 5GB+                                      | 5GB+ (SSD Recommended)                    |
| **OS**            | Windows 10/11, Linux, macOS               | Windows 10/11, Linux                      |

### Mobile (via Termux or similar apps)

| Component         | Minimum                                   |
|-------------------|-------------------------------------------|
| **Device RAM**    | 8GB                                       |
| **Storage**       | 5GB+ Free Space                           |
| **OS**            | Android 10+                               |
| **Processor**     | Modern 8-core CPU (e.g., Snapdragon 7xx+) |

*Note: Performance on mobile devices will be slower than on a desktop with a dedicated GPU.*

---

## 🚀 Example Usage

```python
# Ensure you have the latest transformers and supporting libraries installed
# pip install -U transformers accelerate bitsandbytes

from transformers import AutoTokenizer, AutoModelForCausalLM
import torch

# Path to your local model or Hugging Face repo
model_path = "MAHAVEER-AI/Bol-AI-v1.0"

tokenizer = AutoTokenizer.from_pretrained(model_path, trust_remote_code=True)
model = AutoModelForCausalLM.from_pretrained(
    model_path,
    torch_dtype=torch.bfloat16,
    device_map="auto",
    trust_remote_code=True
)

# Prepare the prompt
prompt = "User: Who is the developer of Bol-AI?\nBol-AI:"

inputs = tokenizer(prompt, return_tensors="pt").to(model.device)

# Generate a response
outputs = model.generate(
    **inputs,
    max_new_tokens=120,
    temperature=0.2,
    do_sample=True
)

response = tokenizer.decode(outputs, skip_special_tokens=True)
print(response.split("Bol-AI:")[-1].strip())
```


# 🔥 Why Bol-AI?

Bol-AI was designed to provide:
- Better conversational intelligence
- Smart assistant interaction
- Enhanced communication quality
- Human-like AI responses
- Optimized assistant behavior
- Lightweight AI deployment
- Personalized AI interaction
- Fast and intelligent responses

The project combines conversational optimization, assistant engineering, and AI response tuning into a single intelligent assistant system.

---

# 🧾 Additional Information

| Information | Details |
|---|---|
| AI Project | Bol-AI |
| Developer Alias | MAHAVEER AI |
| Model Format | SafeTensors |
| Response Style | Conversational |
| Deployment Support | Local / Cloud |
| AI Category | Assistant AI |
| Optimization | Fine-tuned |
| Main Purpose | Intelligent Conversations |
| Assistant Type | Conversational Assistant |
| AI Identity | Bol-AI |
| AI Communication | Optimized |

---

# 🔒 License

Bol-AI includes custom conversational tuning, assistant optimization, response engineering, and fine-tuning developed by Vivek Vijay Dalvi.

Base Model Credit:

MiniCPM-V-4.6 by OpenBMB — Apache-2.0 License.

---

# 👨‍💻 Developer

Vivek Vijay Dalvi  
Founder & Developer of MAHAVEER AI

Bol-AI is a custom conversational AI assistant developed, engineered, optimized, and enhanced by Vivek Vijay Dalvi.
