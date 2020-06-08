# Autopilot-TensorFlow
A TensorFlow implementation of this [Nvidia paper](https://arxiv.org/pdf/1604.07316.pdf) with some changes. For a summary of the design process and FAQs, see [this medium article I wrote](https://medium.com/@sullyfchen/how-a-high-school-junior-made-a-self-driving-car-705fa9b6e860).

# IMPORTANT
Absolutely, under NO circumstance, should one ever pilot a car using computer vision software trained with this code (or any home made software for that matter). It is extremely dangerous to use your own self-driving software in a car, even if you think you know what you're doing, not to mention it is quite illegal in most places and any accidents will land you in huge lawsuits.

This code is purely for research and statistics, absolutley NOT for application or testing of any sort.

<img src="https://github.com/17011813/Autopilot-TensorFlow/blob/master/2020-04-21%20(15).png" width="90%"></img>

# How to Use
Download the [dataset](https://github.com/SullyChen/driving-datasets) and extract into the repository folder

Use `python train.py` to train the model

Use `python run.py` to run the model on a live webcam feed

Use `python run_dataset.py` to run the model on the dataset

[dataset](https://github.com/SullyChen/driving-datasets) 07/01/2018 Dataset 최신 데이터로 돌릴때 data.txt의 데이터 형식이 달라서 47727.jpg 3.530000,2018-07-01​ 17:51:57:21 ​이렇게 되어있어서 line.split()[0] 하면 3.530000,2018-07-01 이렇게 되기때문에 line.split()[0][0:8]로 써줘서 angle 부분만 입력되어 append 되도록 수정하였습니다.
 `python driving_data.py`코드 에서 14번째 줄에 line.split()[0] ----> line.split()[0][0:8]
 
[dataset](https://github.com/SullyChen/driving-datasets)에서 Dataset 1을 쓴다면 코드 수정없이 그대로 해도 됩니다.


To visualize training using Tensorboard use `tensorboard --logdir=./logs`, then open http://0.0.0.0:6006/ into your web browser.

<img src="https://github.com/17011813/Autopilot-TensorFlow/blob/master/hyp.PNG" width="90%"></img>
