# Deep Supervised Discrete Hashing

论文[Deep Supervised Discrete Hashings](http://papers.nips.cc/paper/6842-deep-supervised-discrete-hashing)

## Requirements
1. pytorch 1.1
2. loguru

## 数据集下载
1. [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html)
2. [NUS-WIDE](https://pan.baidu.com/s/1S1ZsYCEfbH5eQguHs8yG_w)
密码：4839

## 运行
`python run.py --dataset cifar10 --data-path <data_path> --code-length 64 `

日志记录在`logs`文件夹内

生成的hash code保存在`result`文件夹内，Tensor形式保存

## 参数说明
```
DSDH_PyTorch

optional arguments:
  -h, --help            show this help message and exit
  --dataset DATASET     Dataset used to train (default: cifar10)
  --data-path DATA_PATH
                        Path of cifar10 dataset
  --num-query NUM_QUERY
                        Number of query(default: 1000)
  --num-train NUM_TRAIN
                        Number of train(default: 5000)
  --code-length CODE_LENGTH
                        Binary hash code length (default: 12)
  --topk TOPK           Compute map of top k (default: 5000)
  --evaluate-freq EVALUATE_FREQ
                        Frequency of evaluate (default: 10)
  --max-iter MAX_ITER   Maximum iteration (default: 150)
  --dcc-iter DCC_ITER   Dcc iteration with one epoch
  --model MODEL         CNN model(default: alexnet)
  --multi-gpu           Use multiple gpu
  --gpu GPU             Use gpu(default: 0. -1: use cpu)
  --lr LR               Learning rate(default: 1e-5)
  --batch-size BATCH_SIZE
                        Batch size(default: 256)
  --num-workers NUM_WORKERS
                        Number of workers(default: 0)
  --nu NU               Hyper-parameter (default: 0.1)
  --mu MU               Hyper-parameter (default: 1)
  --eta ETA             Hyper-parameter (default: 55)

```
