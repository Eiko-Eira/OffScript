# OTTER 8B (Wave 1) 

OTTER 1.0 is a fine-tuned Llama-3.1-8B model specialized for Printed Circuit Board (PCB) design, semiconductor physics, and hardware description languages (Verilog).

## Model Details
Base Model: Meta-Llama-3.1-8B-Instruct
Training Method: LoRA (Rank 128)
Datasets: ElectricalElectronicsIR, ElectricalNER, STEM-AI
Loss average: 0.6 (Wave 1)

## Performance
OTTER excels at:
  Signal Integrity analysis (Via stubs, reflections)
  Component selection (LDO stability, ESR logic)
  Verilog module generation

## How to use
```python
from unsloth import FastLanguageModel
model, tokenizer = FastLanguageModel.from_pretrained("your-username/OTTER-8b-Wave1")
```
### 5. Handling Large Files (Git LFS)
If you decide to keep the `adapter_model.safetensors` directly on GitHub, you **must** use **Git LFS (Large File Storage)**. 
Run these commands in your terminal before pushing:
```bash
git lfs install
git lfs track "*.safetensors"
git add .gitattributes
git add adapter_model.safetensors
```
