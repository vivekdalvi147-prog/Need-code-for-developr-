# 🤖 Bol-AI

<p align="center">
  <img src="https://i.ibb.co/s9X3yR1f/In-Shot-20260117-214933669.jpg" width="220" alt="Bol-AI Logo"/>
</p>

<h1 align="center">Bol-AI</h1>

<h3 align="center">
Custom Conversational AI Assistant
</h3>

<p align="center">
  Developed by Vivek Vijay Dalvi • MAHAVEER AI
</p>

<p align="center">
  <img src="https://i.ibb.co/67Y0XcyV/v-1.png" width="750" alt="India Flag Banner"/>
</p>

---

# 📌 Overview

Bol-AI is a custom conversational AI assistant developed and fine-tuned by Vivek Vijay Dalvi under MAHAVEER AI.

The project focuses on:
- Intelligent conversations
- Assistant personality systems
- Smart response generation
- Enhanced conversational behavior
- Multi-language communication
- Optimized AI interaction
- Human-like AI conversations
- Fine-tuned conversational intelligence

---

# 🌐 Official Documentation

https://bol-ai-docs.web.app

---

# 🧠 Model Information

| Property | Details |
|---|---|
| Model Name | Bol-AI |
| Developer | Vivek Vijay Dalvi |
| Organization | MAHAVEER AI |
| Base Model | MiniCPM-V-4.6 |
| Base Model Developer | OpenBMB |
| Parameters | 1.7 Billion |
| Context Length | 32K Tokens |
| Approx Token Support | 32,000 Tokens |
| Model Size | 2.42 GB |
| Architecture | Transformer |
| Model Format | SafeTensors |
| AI Type | Conversational Assistant |
| Primary Language | English |
| Supported Languages | English, Marathi, Hindi |
| Quantization | Optimized |
| Deployment | Local & Cloud |
| Inference Type | Text Generation |
| License | Apache-2.0 |

---

# 🚀 Advanced Features

- Intelligent conversational responses
- Custom AI personality system
- Human-like communication
- Multi-language understanding
- Fast text generation
- Assistant identity system
- Fine-tuned conversational behavior
- Smart response engineering
- Optimized AI interaction
- Enhanced assistant communication
- Context-aware conversations
- Lightweight deployment support
- Transformer neural architecture
- Dynamic conversational flow
- AI-powered assistant behavior
- Conversational optimization
- Enhanced response quality
- Instruction-following capability
- Smart conversational intelligence
- Optimized inference performance

---

# 📈 Model Capabilities

| Capability | Supported |
|---|---|
| Conversational AI | Yes |
| Question Answering | Yes |
| Multi-language Support | Yes |
| Context Awareness | Yes |
| Smart Responses | Yes |
| Personality System | Yes |
| Assistant Identity | Yes |
| Instruction Following | Yes |
| Long-form Responses | Yes |
| Local Deployment | Yes |
| Cloud Deployment | Yes |
| Lightweight Inference | Yes |
| AI Personality Tuning | Yes |
| Conversational Optimization | Yes |

---

# 🛠️ Training & Customization

Bol-AI includes:
- Conversational fine-tuning
- Personality enhancement
- Response optimization
- Assistant behavior tuning
- Identity engineering
- Additional conversational datasets
- Smart interaction improvements
- AI communication optimization
- Conversational response tuning
- Human-like interaction enhancement

---

# 🧬 Architecture Details

| Specification | Value |
|---|---|
| AI Category | Large Language Model |
| Base Architecture | Transformer |
| Parameter Count | 1.7B |
| Quantization | Optimized |
| Deployment Style | Local & Cloud |
| Inference Type | Text Generation |
| Main Weight File | model.safetensors |
| Model Framework | Transformers |

---

# 📂 Repository Structure

```text
mahaveerai/bol-ai
│
├── model.safetensors
├── config.json
├── tokenizer.json
├── tokenizer_config.json
├── generation_config.json
├── special_tokens_map.json
├── README.md
```

---

# 💻 Recommended Requirements

| Component | Recommended |
|---|---|
| GPU VRAM | 6GB+ |
| RAM | 16GB+ |
| Python | 3.10+ |
| CUDA | Supported |

---

# 🚀 Example Usage

```python
from transformers import AutoTokenizer, AutoModelForCausalLM

model_path = "mahaveerai/bol-ai"

tokenizer = AutoTokenizer.from_pretrained(model_path)
model = AutoModelForCausalLM.from_pretrained(model_path)

prompt = "Hello Bol-AI"

inputs = tokenizer(prompt, return_tensors="pt")

outputs = model.generate(
    **inputs,
    max_new_tokens=100
)

print(tokenizer.decode(outputs[0], skip_special_tokens=True))
```

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

---

# 🔒 License

Bol-AI includes custom modifications, conversational tuning, and fine-tuning developed by Vivek Vijay Dalvi.

Base Model Credit:

MiniCPM-V-4.6 by OpenBMB — Apache-2.0 License.

---

# 👨‍💻 Developer

Vivek Vijay Dalvi  
Founder of MAHAVEER AI

Bol-AI is a custom conversational AI assistant developed and enhanced by Vivek Vijay Dalvi.
