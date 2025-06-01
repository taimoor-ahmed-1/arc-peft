---

## 📚 Requirements

This project is designed to run in **Google Colab** with an **A100 GPU**.

Required Python packages:

- `transformers`
- `datasets`
- `peft`
- `bitsandbytes` (optional if using 8-bit/4-bit quantization)
- `torch`
- `matplotlib`
- `scikit-learn`

👉 The notebook will install all required libraries automatically.

---

## 🚀 How to Run in Google Colab

### 1️⃣ Open the notebook in Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

Or manually upload `lora_fs_arc_final.ipynb` to Colab.

---

### 2️⃣ Enable GPU:

- Go to **Runtime** → **Change runtime type** → Select **GPU** (preferably **A100**).

---

### 3️⃣ Run the notebook step-by-step:

#### Sections:

✅ Install dependencies  
✅ Load ARC Challenge dataset  
✅ Load Qwen-7B-Chat model  
✅ Apply LoRA and fine-tune  
✅ Save LoRA adapter to Google Drive  
✅ Run Few-shot evaluation  
✅ Load LoRA adapter and run LoRA evaluation  
✅ Plot results and compare

---

## 💾 Saving Outputs

- **LoRA adapters** are saved to your Google Drive under `/content/drive/MyDrive/lora_adapter_arc/`.
- You can later reload them using `PeftModel.from_pretrained`.

---

## 📊 Outputs

The notebook will generate:

- Accuracy for Few-shot and LoRA
- Macro F1-score for Few-shot and LoRA
- Inference latency comparison
- Confusion matrix for each method
- LoRA training loss curve

---

## ✏️ Notes

- If you get **OutOfMemory errors**, ensure you're using an **A100 GPU** and clear CUDA cache between stages.
- LoRA training requires some VRAM (~30-35GB for Qwen-7B on A100).
- Few-shot inference is lighter but less accurate.

---

## 📈 Example Results

| Metric                  | Few-shot Learning | LoRA Fine-Tuning |
|-------------------------|-------------------|------------------|
| Accuracy                | 66.58%            | 77.48%           |
| Macro F1-score          | 56.67%            | 63.00%           |
| Inference Latency       | 0.2487 sec/sample | 0.5580 sec/sample|

---

## 🏆 Conclusion

- **LoRA Fine-Tuning** achieves significantly better accuracy and balanced performance.
- **Few-shot Learning** is faster to set up but depends heavily on prompt quality.
- LoRA is preferred when accuracy is critical; Few-shot is useful for quick prototyping.

---

## 🤝 Acknowledgments

- ARC Dataset: Clark et al. (2018)
- LoRA: Hu et al. (2021)
- Qwen-7B-Chat by Alibaba Cloud

---

## 🔗 References

- [ARC Dataset](https://allenai.org/data/arc)
- [LoRA paper](https://arxiv.org/abs/2106.09685)
- [Qwen Models](https://huggingface.co/Qwen)

---