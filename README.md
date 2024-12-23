# Illustrious XL Basic

## LandScape(3:2 [1824 x 1248])
![image](./landscape/workflow.png)

## Portait(2:3 [1248 x 1824])
![image](./portait/workflow.png)

## Setup
- Python 3.12.3
```bash
cd ComfyUI
pip install -r requirements.txt
pip install websocket-client

cd models/checkpoints
wget https://huggingface.co/OnomaAIResearch/Illustrious-xl-early-release-v0/resolve/main/Illustrious-XL-v0.1.safetensors

cd custom_nodes
git clone https://github.com/KohakuBlueleaf/z-tipo-extension.git

```

## Example
### LandScape
```bash
time python main.py --mode 1 --prompt "Yumekawa Tenshi's cute angel is flying in the winter sky" --save_path "./test.png"
```
NVIDIA L40S
```
real    0m15.321s
user    0m1.068s
sys     0m0.020s
```

### Portait
```bash
time python main.py --mode 2 --prompt "Yumekawa Tenshi's cute angel is flying in the winter sky" --save_path "./test.png"
```
NVIDIA L40S
```
real    0m15.333s
user    0m1.063s
sys     0m0.010s
```


