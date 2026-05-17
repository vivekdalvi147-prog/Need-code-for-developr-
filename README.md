# 🤖 Bol-AI

<p align="center">
  <img src="https://i.ibb.co/s9X3yR1f/In-Shot-20260117-214933669.jpg" width="220" alt="Bol-AI Logo"/>
</p>

<p align="center">
  <b>Bol-AI — Custom Conversational AI Assistant</b>
</p>

<p align="center">
  <img src="https://i.ibb.co/67Y0XcyV/v-1.png" width="320" alt="Bol-AI India Banner"/>
</p>

---

# 📌 Overview

Bol-AI is a custom AI assistant developed and fine-tuned by Vivek Vijay Dalvi under MAHAVEER AI.

The model has been customized with:

* Additional conversational training
* Personality enhancement
* AI response optimization
* Assistant behavior tuning
* Custom identity system
* Improved communication style
* Enhanced conversational intelligence

Bol-AI is designed to provide fast, intelligent, and natural conversations while maintaining a custom assistant identity.

---

# 🧠 Model Information

| Property             | Details                     |
| -------------------- | --------------------------- |
| Model Name           | Bol-AI                      |
| Developer            | Vivek Vijay Dalvi           |
| Organization         | MAHAVEER AI                 |
| Base Model           | MiniCPM-V-4.6               |
| Model Type           | Conversational AI Assistant |
| Parameters           | 1.7 Billion                 |
| Context Length       | 32K Tokens                  |
| Approx Token Support | 32,000 Tokens               |
| Model Weight Size    | 2.42 GB                     |
| Model Size           | 2.42 GB                     |
| Primary Language     | English                     |
| Supported Languages  | English, Marathi, Hindi     |
| Architecture         | Transformer-based           |
| License              | Apache-2.0                  |

---

# 🌐 Official Documentation

Documentation Website:
[https://bol-ai-docs.web.app](https://bol-ai-docs.web.app)

---

# 🌟 Key Highlights

* Custom conversational AI assistant
* Enhanced personality-based responses
* Optimized assistant communication system
* Fine-tuned conversational behavior
* Intelligent multi-language interaction
* Custom identity engineering
* Fast and lightweight deployment
* Transformer-based architecture
* Optimized for assistant-style conversations

---

# 🚀 Advanced AI Features

* Intelligent conversational reasoning
* Assistant personality system
* Multi-language understanding
* Human-like response generation
* Fast text generation
* Smart instruction following
* Conversational optimization
* Context-aware replies
* AI identity system
* Fine-tuned response behavior
* Assistant communication tuning
* Natural language processing
* Lightweight deployment support
* Optimized inference performance
* Enhanced interaction handling
* Transformer neural architecture
* Custom response engineering
* Dynamic assistant behavior
* AI-powered communication
* Smart conversational flow

---

# ⚡ Features

* Intelligent conversational responses
* Custom AI identity system
* Fast response generation
* Personality-based assistant behavior
* Fine-tuned communication style
* Multi-language support
* Optimized assistant interaction
* Enhanced conversational memory behavior
* Custom response engineering

---

# 📈 Model Capabilities

| Capability               | Availability |
| ------------------------ | ------------ |
| Chat & Conversation      | Yes          |
| Question Answering       | Yes          |
| Multi-language Support   | Yes          |
| AI Personality System    | Yes          |
| Context Awareness        | Yes          |
| Smart Responses          | Yes          |
| Assistant Identity       | Yes          |
| Instruction Following    | Yes          |
| Lightweight Deployment   | Yes          |
| Fine-tuned Communication | Yes          |

---

# 📊 Performance Information

| Capability                | Status    |
| ------------------------- | --------- |
| Conversational AI         | Supported |
| Multi-language Responses  | Supported |
| Personality Responses     | Supported |
| Assistant Identity System | Enabled   |
| Smart Prompt Handling     | Enabled   |
| Instruction Following     | Optimized |
| Long-form Responses       | Supported |
| Lightweight Deployment    | Supported |

---

# 🛠️ Training & Customization

Bol-AI was customized and enhanced by:

* Fine-tuning conversational behavior
* Additional response training
* Identity engineering
* Personality optimization
* Assistant response improvements
* Smart conversational enhancements
* Custom AI behavior alignment

---

# 🧬 Architecture Details

| Specification     | Value                |
| ----------------- | -------------------- |
| AI Category       | Large Language Model |
| Base Architecture | Transformer          |
| Parameter Count   | 1.7B                 |
| Quantization      | Optimized            |
| Model Format      | SafeTensors          |
| Main Weight File  | model.safetensors    |
| Deployment Style  | Local & Cloud        |
| Inference Type    | Text Generation      |

---

# 📂 Model Files

| File                    | Description             |
| ----------------------- | ----------------------- |
| model.safetensors       | Main model weights      |
| tokenizer.json          | Tokenizer configuration |
| tokenizer_config.json   | Tokenizer settings      |
| config.json             | Model configuration     |
| generation_config.json  | Generation parameters   |
| special_tokens_map.json | Special token mappings  |
| README.md               | Model documentation     |

---

# 🚀 Usage

Example usage:

```python
from transformers import AutoTokenizer, AutoModelForCausalLM

model_path = "mahaveerai/bol-ai"

tokenizer = AutoTokenizer.from_pretrained(model_path)
model = AutoModelForCausalLM.from_pretrained(model_path)

prompt = "Hello Bol-AI"
inputs = tokenizer(prompt, return_tensors="pt")

outputs = model.generate(**inputs, max_new_tokens=100)
print(tokenizer.decode(outputs[0], skip_special_tokens=True))
```

---

# 📦 Repository Structure

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
| --------- | ----------- |
| GPU VRAM  | 6GB+        |
| RAM       | 16GB+       |
| Python    | 3.10+       |
| CUDA      | Supported   |

---

# 🔒 License

This project includes custom fine-tuning and modifications developed by Vivek Vijay Dalvi.

Base model credit:
MiniCPM-V-4.6 by OpenBMB — Apache-2.0 License.

---

# 🧾 Additional Information

| Information        | Details                   |
| ------------------ | ------------------------- |
| AI Project         | Bol-AI                    |
| Developer Alias    | MAHAVEER AI               |
| Model Format       | SafeTensors               |
| Response Style     | Conversational            |
| Deployment Support | Local / Cloud             |
| AI Category        | Assistant AI              |
| Optimization       | Fine-tuned                |
| Main Purpose       | Intelligent Conversations |

---

# 🔥 About Bol-AI

Bol-AI is designed to deliver natural and intelligent AI conversations with enhanced assistant behavior and custom conversational tuning.

The project focuses on:

* Assistant intelligence
* Human-like responses
* Identity-based AI interaction
* Smart conversational behavior
* AI communication optimization

---

# 👨‍💻 Developer

Vivek Vijay Dalvi
Founder of MAHAVEER AI

Bol-AI is a custom conversational AI assistant developed and enhanced by Vivek Vijay Dalvi.
