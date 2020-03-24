# Python Code Library

## Tensorflow

### Tensorboard

```python
from Mar_2020_words.Code.main.Words.GlobalVariables import *
import sys

# To use tensorboard, run the following code in the terminal
print(f"tensorboard --logdir {Path_folder_log} --host localhost --port 8088")
sys.exit()
```

## Jupyter

### Drawing

#### Show imgs under specific folder in the unit

```python
from IPython.core.display import Image
from pylab import *
def fig(s): return Image(filename="Figures-intro/"+s+".png")
def figs(*args,**kw):
    rs = kw.get("rows",1)
    cs = kw.get("cols",len(args))
    for i,f in enumerate(args):
        subplot(rs,cs,i+1)
        axis("off")
        imshow(imread("Figures-intro/"+f+".png"))
from scipy.ndimage import filters
```

when applying

```python
# Color Constancy Revealed
figs("cc1","cc2","cc3","cc4",rows=2,cols=2)
```

