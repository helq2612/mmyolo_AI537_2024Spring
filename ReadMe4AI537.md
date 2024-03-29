## Install conda


## Install mmyolo and dependency libraries
Install MMYOLO and dependency libraries using the following commands.
For details about how to configure the environment, see [Installation and verification](https://mmyolo.readthedocs.io/en/latest/get_started/installation.html).
```{note}
Note: Since this repo uses OpenMMLab 2.0, it is better to create a new conda virtual environment to prevent conflicts with the repo installed in OpenMMLab 1.0.
```

```shell
conda remove --name myenv --all -y 
conda create --name myenv python=3.8 -y
conda activate myenv

# install Pytorch
pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cu118
python -c 'import torch;print(torch.__version__)'

# pull the repository from github
git clone https://github.com/helq2612/mmyolo_AI537_2024Spring.git


# install dependency libraries
cd mmyolo_AI537_2024Spring
pip install -U openmim
mim install -r requirements/mminstall.txt
mim install -r requirements/albu.txt

# compile mmyolo
pip install -v -e .
# or use this command
mim install -v -e .

# install jupyter lab
pip install jupyterlab
```

