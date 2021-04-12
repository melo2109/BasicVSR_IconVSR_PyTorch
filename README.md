##  Dependencies and Installation
- The code is based on [BasicSR](https://github.com/xinntao/BasicSR), please follow the requirements of BasicSR.
- Pytorch=1.51

##  Training
```bash
CUDA_VISIBLE_DEVICES=0,1 python basicsr/train.py -opt options/train/BasicVSR/train_BasicVSR.yml

CUDA_VISIBLE_DEVICES=0,1 python basicsr/train.py -opt options/train/BasicVSR/train_IconVSR.yml
```
## Testing
```bash
CUDA_VISIBLE_DEVICES=0 python basicsr/test.py -opt options/test/BasicVSR/test_BasicVSR_REDS.yml

CUDA_VISIBLE_DEVICES=0 python basicsr/test.py -opt options/test/BasicVSR/test_BasicVSR_Vid4.yml
```

## PSNR Results
It takes about 5 days to train the BasicVSR/IconVSR model on 2 V100 GPUs.

| Dataset(BI) | BasicVSR (paper) | Ours |IconVSR (paper) | Ours |
| :----- | :-----: | :-----: | :-----: | :-----: | 
| REDS4 | 31.42 | 31.4096 | - | - |
| Vid4 | 27.24 |27.2693| - | - |
