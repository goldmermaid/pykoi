
# :whale2: pykoi: Active learning in one unified interface :ocean:!
<p align="center">
  <a href="/LICENSE"><img alt="License Apache-2.0" src="https://img.shields.io/github/license/cambioml/pykoi?style=flat-square"></a>
  <a href="https://pypi.org/project/pykoi"><img src="https://img.shields.io/pypi/v/pykoi.svg" alt="pypi_status" /></a>
  <a href="https://github.com/cambioml/pykoi/graphs/commit-activity"><img alt="Commit activity" src="https://img.shields.io/github/commit-activity/m/cambioml/pykoi?style=flat-square"/></a>
  <a href="https://join.slack.com/t/cambiomlworkspace/shared_invite/zt-1zes33rmt-20Rag043uvExUaUdvt5_xQ"><img src="https://badgen.net/badge/Join/Community/cyan?icon=slack" alt="Slack" /></a>
</p>

## :seedling: Installation
To get started to `pykoi`, we recommend you test on an EC2 instance instance with the following config:
- EC2 `g5.2x` (if you want to run a pretrained model with 7B parameters)
- Deep Learning AMI GPU PyTorch 2.0.1 (Ubuntu 20.04) 20230627
- EBS: at least 100G

Once you are on your EC2 terminal, create a conda environment using:
```
conda create -n pykoi python=3.10 -y && source activate pykoi
```

Then install `pykoi` and the correlated torch version.
```
pip3 install pykoi && pip3 install torch --index-url https://download.pytorch.org/whl/cu118
```

## :question: How do I use `pykoi`?

`pykoi` is a python interface to unify your ML model development and production. You can easily get real-time user feedback and continuous improving your model. 

Here are some examples of common applications:

### :speech_balloon: Chatbots

- If you are on a GPU instance, check [launch_app_gpu.ipynb](example/notebook/launch_app_gpu.ipynb) and see how to launch a chatbot UI using multiple models, and thumb up/down the model answers side by side.
- If you are on a CPU instance, check [launch_app_api.ipynb](example/notebook/launch_app_api.ipynb) and see how to launch a chatbot UI using OpenAI or Amazon Bedrock (:woman_technologist: building now :man_technologist:), and thumb up/down the model answers side by side.


## :nerd_face: Dev Setup
If you are interested to contribute to us, here are the preliminary development setup.

### Backend Dev Setup
```
conda create -n pykoi python=3.10
conda activate pykoi
cd pykoi
pip3 install poetry
poetry install --no-root
```

### Frontend Dev Setup
Frontend:
```
cd frontend
npm instal vite
npm run build
```
