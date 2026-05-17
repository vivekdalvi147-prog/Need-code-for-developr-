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
# ==============================================================================
# BOL-AI v1.0 PRO - OFFICIAL EXECUTION SCRIPT
# Developer: Vivek Vijay Dalvi | Company: MAHAVEER AI
# ==============================================================================

# SYSTEM REQUIREMENTS:
# 1. Python 3.10 or higher installed.
# 2. Minimum 8GB RAM (16GB recommended).
# 3. Active internet connection for the first run to download weights (2.42 GB).

# INSTALLATION COMMAND:
# Run this in your terminal before starting the script:
# pip install torch transformers accelerate bitsandbytes sentencepiece

import torch
import os
from transformers import AutoTokenizer, AutoModel

# Set environment variable for Windows UTF-8 support
os.environ["PYTHONUTF8"] = "1"

# Official Hugging Face Repository ID
MODEL_ID = "mahaveerai/bol-ai"

# AI Inference Settings
GEN_TEMPERATURE = 0.2
MAX_NEW_TOKENS = 300

def initialize_engine():
    """Load tokenizer and model weights from the repository"""
    print("Initializing Bol-AI v1.0 Pro Engine...")
    try:
        # Load tokenizer with remote code trust enabled
        tokenizer = AutoTokenizer.from_pretrained(MODEL_ID, trust_remote_code=True)
        
        # Load model weights in BFloat16 precision for efficiency
        model = AutoModel.from_pretrained(
            MODEL_ID,
            torch_dtype=torch.bfloat16,
            device_map="auto",
            trust_remote_code=True
        )
        model.eval()
        return tokenizer, model
    except Exception as e:
        print(f"Error during initialization: {e}")
        return None, None

def start_chat(tokenizer, model):
    """Main conversation interface"""
    print("\n" + "="*40)
    print("BOL-AI v1.0 PRO IS ONLINE")
    print("Developer: Vivek Vijay Dalvi")
    print("Company: MAHAVEER AI")
    print("="*40)
    print("Type 'exit' or 'quit' to end the session.\n")

    while True:
        user_input = input("You: ")
        if user_input.lower() in ["exit", "quit"]:
            print("Bol-AI: Session terminated.")
            break

        # Prepare message format for MiniCPM architecture
        messages = [{"role": "user", "content": user_input}]
        
        print("Bol-AI: Thinking...", end="\r")
        
        try:
            # Attempt optimized chat inference
            response = model.chat(
                image=None,
                msgs=messages,
                tokenizer=tokenizer,
                sampling=True,
                temperature=GEN_TEMPERATURE,
                top_p=0.9
            )
            print(f"Bol-AI: {response}\n")
            
        except Exception:
            # Fallback to standard autoregressive generation if chat fails
            prompt = f"User: {user_input}\nBol-AI:"
            inputs = tokenizer(prompt, return_tensors="pt").to(model.device)
            
            with torch.no_grad():
                outputs = model.generate(
                    **inputs, 
                    max_new_tokens=MAX_NEW_TOKENS,
                    pad_token_id=tokenizer.eos_token_id
                )
            
            decoded_output = tokenizer.decode(outputs[0], skip_special_tokens=True)
            # Extract only the AI response part
            final_text = decoded_output.split("Bol-AI:")[-1].strip()
            print(f"Bol-AI: {final_text}\n")

if __name__ == "__main__":
    # Start the application
    tk, md = initialize_engine()
    if tk and md:
        start_chat(tk, md)
    else:
        print("Failed to start Bol-AI. Please check your installation and connection.")
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
