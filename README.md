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


import sys

from cclib.method import MPA
from cclib.parser import ccopen

d = ccopen(sys.argv[1]).parse()
m = MPA(d)
m.calculate()


from cclib.method import MPA
from cclib.parser import ccopen
from cclib.progress import TextProgress
import logging

progress = TextProgress()
d = ccopen("mycalc.out", logging.ERROR).parse(progress)

m = MPA(d, progres, logging.ERROR)
m.calculate()



import sys

from cclib.method import LPA
from cclib.parser import ccopen

d = ccopen(sys.argv[1]).parse()
m = LPA(d)
m.calculate()


from cclib.parser import ccopen
from cclib.method import Density

parser = ccopen("myfile.out")
data = parser.parse()

d = Density(data)
d.calculate()


import sys

from cclib.parser import ccopen
from cclib.method import MBO

parser = ccopen(sys.argv[1])
data = parser.parse()

d = MBO(data)
d.calculate()

from cclib.io import ccopen
from cclib.method import CDA

molecule = ccopen("molecule.log")
frag1 = ccopen("fragment1.log")
frag2 = ccopen("fragment2.log")

m = molecule.parser()
f1 = frag1.parse()
f2 = frag2.parse()

cda = CDA(m)
cda.caluculate([f1, f2])
```

```sh
ccget atomcharges Benzeneselenol.out
ccget scfenergies Benzenselenol.out
```

```
```


