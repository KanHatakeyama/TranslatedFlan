# [FLAN dataset](https://huggingface.co/datasets/Open-Orca/FLAN)から日本語訳を自動生成するコード

# Setup FLAN dataset
~~~
export GIT_LFS_SKIP_SMUDGE=1
git clone https://huggingface.co/datasets/Open-Orca/FLAN
cd FLAN
git lfs pull 
git lfs checkout
~~~

# Environment
~~~
conda create -n synthtext python=3.11 -y
conda activate synthtext

pip install vllm==0.4.2
pip install datasets==2.19.1
~~~

# Launch
~~~
conda activate synthtext
# 下記ファイル中､directory_path = '/data/2024/FLAN/'を設定すること
pythn 0624translate_flan.py
~~~