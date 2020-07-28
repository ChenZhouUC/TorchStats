# Inherited Repo from torchstat
### (Transplanted for EdgeNNWorkshop)

![torchstats](https://github.com/ChenZhouUC/TorchStats/blob/master/assets/torchstats.png)

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