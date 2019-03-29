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


```

```sh
ccget atomcharges Benzeneselenol.out
ccget scfenergies Benzenselenol.out
```

```
```


