LoRA vs Few-shot Learning for MCQA on ARC Dataset

This project compares Few-shot Learning and Low-Rank Adaptation (LoRA) fine-tuning for solving Multiple-Choice Question Answering (MCQA) on the ARC Challenge dataset using the Qwen-7B-Chat model.

⸻

Project Structure

lora_fewshot_arc_452257.ipynb   # Main notebook (run this in Colab)
README.md                 # Project README
saved_lora_adapter/       # LoRA adapter saved to Google Drive


⸻

Requirements

This project is designed to run in Google Colab with an A100 GPU.

Required Python packages:
	•	transformers
	•	datasets
	•	peft
	•	bitsandbytes (optional)
	•	torch
	•	matplotlib
	•	scikit-learn

The notebook installs all required libraries automatically.

⸻

How to Run in Google Colab
	1.	Open the notebook in Colab:
Upload lora_fewshot_arc_452257.ipynb to Google Colab.
	2.	Enable GPU:
Runtime → Change runtime type → Select GPU (A100 preferred).
	3.	Run the notebook step-by-step:

	•	Install dependencies
	•	Load ARC dataset
	•	Load Qwen-7B-Chat model
	•	Apply LoRA and fine-tune
	•	Save LoRA adapter
	•	Run Few-shot evaluation
	•	Run LoRA evaluation
	•	Compare results

⸻

Saving Outputs
	•	LoRA adapters will be saved to your Google Drive at:
/content/drive/MyDrive/lora_adapter_arc/

⸻

Example Results

Metric	Few-shot Learning	LoRA Fine-Tuning
Accuracy	66.58%	77.48%
Macro F1-score	56.67%	63.00%
Inference Latency	0.2487 sec/sample	0.5580 sec/sample


⸻

Conclusion
	•	LoRA Fine-Tuning achieves higher accuracy and balanced performance.
	•	Few-shot Learning is faster to set up but depends on prompt quality.
	•	LoRA is better for accuracy-critical applications.

⸻

References
	•	ARC Dataset: Clark et al. (2018)
	•	LoRA paper: Hu et al. (2021)
	•	Qwen Models: Alibaba Cloud

⸻
