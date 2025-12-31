## How to Install Environment (Using Conda)
conda create -n cvdl_hw1 python=3.10 -y
conda activate cvdl_hw1
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
python -c "import torch; print(torch.cuda.is_available(), torch.version.cuda)" # to verify GPU driver is setup correctly (should be 'True 12.1')

pip freeze > requirements.txt
pip install -r requirements.txt
conda install notebook
jupyter-notebook


## How to Run Training

## How to Run Training


