# DL-Chexpert-Project

This project uses a **DenseNet-based convolutional neural network** trained on the **CheXpert dataset** to classify chest X-ray images for three diagnoses:
- **Pleural Effusion**
- **Edema**
- **Cardiomegaly**

The app includes:
- Grad-CAM visualizations to interpret model attention  
- Diagnosis confidence summary  
- Deployed with **Gradio** and **Hugging Face Spaces**

---

## Folder Structure

```
DL-Chexpert-Project/
│
├── chexpert_gradio_app/        ← Gradio demo app
│   ├── app.py                   ← Main Gradio script
│   ├── final_model.keras        ← Trained model file
│   ├── requirements.txt         ← Python dependencies
│   └── examples/                ← Example chest X-rays
│
├── notebooks/                   ← Model training, evaluation, EDA
│   └── final_model.ipynb        ← Notebook to train model
│
├── report/                      ← Written report (PDF or DOCX)
│   └── Diagnosing Chest Diseases Using convolutional neural networks.pdf
│
├── .gitignore                   ← Excludes model files or logs
└── README.md                    ← You're here!
```


---

## LIVE DEMO
    VISIT: https://sindrem-chexpert-gradio.hf.space/

---



## How to Run Locally

1. **Clone the repo**  
```bash
git clone https://github.com/h669780/DL-Chexpert-Project.git
cd DL-Chexpert-Project/chexpert_gradio_app
```

2. **Install dependencies**  
```bash
pip install -r requirements.txt
```

3. **Launch the app**  
```bash
python app.py
```

4. Visit `http://localhost:7860` in your browser.

---


## Deploying to Hugging Face Spaces yourself

1. Create a Space:  
   - Type: `Gradio`
   - SDK: `Gradio`
2. Upload:
   - `app.py`
   - `final_model.keras`
   - `requirements.txt`
   - `examples/` folder
3. Hugging Face will automatically detect and run `app.py`.

---

## Model Information

- **Architecture:** DenseNet121 (pretrained on ImageNet)
- **Loss:** BinaryFocalLoss (gamma=2)
- **Optimizer:** Adam (`lr=1e-4`)
- **Metrics:** AUC (multi-label)

---

## Demo Instructions

1. Upload a chest X-ray or use one of the example images.
2. Click **Submit**.
3. View:
   - Grad-CAM attention map  
   - Top-3 prediction confidence  
   - Text summary of most likely diagnosis
   
---

