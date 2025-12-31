### Install Conda Environment
conda create -n cvpdl-hw2 python=3.10 -y
conda activate cvpdl-hw2

pip install -r requirements.txt

pip freeze > requirements.txt
pip install -r requirements.txt
conda install notebook
jupyter-notebook

