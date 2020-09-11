# mobilenext.pytorch

MobileNeXt from ECCV20 [paper](https://arxiv.org/abs/2007.02269)

official repo: https://github.com/zhoudaquan/rethinking_bottleneck_design

Third-party repo: https://github.com/d-li14/mobilenext.pytorch

According to this [issue](https://github.com/zhoudaquan/rethinking_bottleneck_design/issues/2#issuecomment-662302401), I changed the hidden layer channels of SGBlock. More details are in `net.log`



## Results

For faster training, I set batch_size=512, initial LR=0.1, other settings are the save with [original paper](https://arxiv.org/abs/2007.02269):

+ WD=5e-4
+ Momentum=0.9
+ totally 200 epochs
+ cosine LR decay with 3 epochs warmup

There is only ONE thing special, I don't use color jiterring when training.

I train this MobileNeXt model with four Tesla V100 GPUs, the best val top-1 is 73.0%, more details please refer to `train.log`.

