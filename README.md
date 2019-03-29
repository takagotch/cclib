### cclib
---
http://cclib.github.io/

```py 
import cclib

filename = "logfile.out"
parser = cclib.io.ccopen(filename)
data = parer.parser()
print("There are %i atoms and %i MOs" % (data.natom, data.nmo))

import cclib

filename = "logfile.out"
data = cclib.io.ccread(filename)
print("There are %i atoms and %i MOs" % (data.natom, data.nmo))


from cclib.io import ccread
from cclib.method import CSPA

data = ccreead("mycalc.out")

m = CSPA(data)
m.calculate()


from cclib.io import ccread
from cclib.method import CSPA

data = ccread("mycalc.out")

m = CSPA(data)
m.calculate([0, 1, 2, 3, 4], [5, 6], [7, 8, 9])


from cclib.method import CSPA
from cclib.parser import Gaussian
from cclib.progress import TextProgress

import logging

progress = TextProgress()
p = Gaussian("mycalc.out", logging.ERROR)
d = p.parse(progress)

m = SCPA(d, progres, logging.ERROR)
m.calculate()

```

```sh
ccget atomcharges Benzeneselenol.out
ccget scfenergies Benzenselenol.out
```

```
```


