# Hackaton-Fashion-Description-Generator
# 🧵 Fashion Description Generator – CPU-Friendly AI Pipeline

## 🎯 Project Objective

Build a lightweight, automated **Generative AI pipeline** that:
- 📝 Generates high-quality, engaging **fashion product descriptions** from an image or keyword (e.g., "robe en soie rouge"),
- 📏 Performs **automated quality checks** (grammar, clarity, coherence),
- 🚫 Applies **ethical filtering** to avoid offensive content or stereotypes,
- ⚙️ Runs efficiently on **CPU-only machines** (no GPU required).

This tool is ideal for fashion e-commerce platforms, designers, or content creators looking to scale product content generation responsibly and efficiently.

---

## 🛠️ Features

- **Input:** Fashion item image or descriptive keyword
- **Output:** A clean, stylish, and market-ready product description
- **Pipeline Components:**
  1. 🔄 Input Parsing (image or keyword)
  2. 🤖 Text Generation (with lightweight model such as DistilGPT-2)
  3. ✨ Quality Check (using NLP tools like spaCy or LanguageTool)
  4. 🛡️ Ethical Filter (custom keyword/stereotype blocklist)
  5. ✅ Final output formatting

---

## ⚙️ Tech Stack

| Component             | Tool/Library                        |
|-----------------------|-------------------------------------|
| Language              | Python                              |
| Text Generation       | 🤖 `transformers` (e.g. DistilGPT2) |
| Image Processing (opt)| `Pillow`, `CLIP` (optional)         |
| Grammar/Style Check   | `spaCy`, `language-tool-python`     |
| Ethical Filtering     | Custom keyword/stereotype filters   |
| Interface (optional)  | `streamlit` or `Flask`              |

---

## 💡 How It Works

1. **User provides** either:
   - A fashion keyword (e.g. “tailleur oversize beige”), or
   - An image of a clothing item.

2. The system:
   - Extracts key attributes (color, type, material)
   - Feeds them into a generative model (e.g. DistilGPT2)
   - Generates a first draft of the product description

3. A **quality checker** runs:
   - Grammar/spelling analysis
   - Readability assessment

4. The description is passed through an **ethical filter**:
   - Detects and blocks stereotypes, sensitive language, or discriminatory terms

5. ✅ The final text is returned to the user, clean and market-ready.

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/fashion-description-generator.git
cd fashion-description-generator

# (Optional) Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app (CLI or Streamlit)
python main.py
```

---

## 🧪 Example

**Input:**
```
"veste en jean oversize"
```

**Output:**
> "Affirmez votre style avec cette veste en jean oversize, au design vintage revisité. Sa coupe ample et ses finitions soignées en font une pièce essentielle pour un look urbain décontracté."

---

## ✅ CPU-Optimized

- Uses **small, fast models** (DistilGPT2 or similar)
- No GPU dependency
- Suitable for lightweight deployments (local machine, small server, edge device)

---

## 📂 Project Structure

```
fashion-description-generator/
│
├── data/                 # Sample images and keywords
├── models/               # Light pretrained models or configs
├── src/
│   ├── generator.py      # Text generation logic
│   ├── quality_check.py  # Grammar/readability checks
│   ├── filter.py         # Ethical filtering rules
│   └── main.py           # Main pipeline script
├── requirements.txt
└── README.md
```

---

## 🔒 Ethical Considerations

This project takes extra care to:
- Avoid **gendered marketing clichés**
- Detect and remove **offensive or biased language**
- Promote **inclusive fashion language**

---

## 📜 License

This project is licensed under the MIT License.

---

## 👩‍💻 Author

Naomie Marciano  
*Fashion & AI Enthusiast*  
[LinkedIn] | [Portfolio]

---

## 🙌 Contributions

Feel free to open issues or submit pull requests to improve the tool or its filters!
