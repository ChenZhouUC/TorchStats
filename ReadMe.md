# Inherited Repo from `torchstat`

<div align=center>
<img src="https://github.com/ChenZhouUC/TorchStats/blob/master/assets/torchstats.png" alt="torchstats" width="250" align="center"/>
</div>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 

This is an inherited repository from the package `torchstat`. I updated it a little for transplantation over `EdgeNNWorkshop`, which is a private project developed for applying neural networks on edge computing cases.

#### Usage

```python
conda activate <pytorch-env>
pip install torchstat # conda install torchstat

# check the torchstat installation position
# overwrite the torchstat dir with files under this repo
cp TorchStats/*.py <torchstat-dir>/torchstat/ 
```

#### Demo

```python
from torchstat import stat
import torchvision.models as models

# make sure this stats tool run with cpu
model = models.resnet18()
# here you can add your own logger with the stat output as info
stat(model, (3, 224, 224), logger=None)
```

#### Improvements

+ The module wrappers are removed after stats are logged so that one can train his own model with either GPU or CPU as he likes.
+ The module buffers are removed so that one can trace the modules and avoid duplicated key errors.
