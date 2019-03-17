### grumpy
---
https://github.com/google/grumpy

```py
""" """
from '' import Args

argv = []
for arg in Args:
  argv.append(arg)
  
goversion = Version()
maxint = MaxInt
maxsize = maxint
maxunicode = Maxint
maxunicode = MaxRune
modules = SysModules
py3kwarning = False
warnoptions = []
byteorder = 'litle'
version = '2.7.13'

class _Flag(object):
  """ """
  debug = 0
  py3k_warning = 0
  division_warning = 0
  division_new = 0
  inspect = 0
  interactive = 0
  optimize = 0
  dont_write_bytecode = 0
  no_user_site = 0
  no_site = 0
  ignore_environment = 0
  tabcheck = 0
  verbose = 0
  unicode = 0
  bytes_warning = 0
  hash_randomization = 0
  
flags = _Flags()

def exc_clear():
  __frame__().__exc_clear__()

def exc_info():
  e, tb = __frame__().__exc_info__()
  t = None
  if e:
    t = type(e)
  return t, e, tb
  
def exit(code=None):
  raise SystemExit(code)

def _getframe(depth=0):
  f = __frame__()
  while depth > 0 and f is not None:
    f = f.f_back
    depth -= 1
  if f is None:
    raise ValueError('call stack is not deep enough')
  return f
```

```
echo "print 'hello, world'" | make run
make
export PATH=$PWD/build/bin:$PATH
export GOPATH=$PWD/build
export PYTHONPATH=$PWD/build/lib/python2.7/site-packages

echo 'import sys; print sys.version' | grumprun
echo 'def hello(): print "hello, world"' > $GOPATH/src/__python__/hello.py

mkdir -p $GOPATH/src/__python__/hello
grumpc -modname=hello $GOPATH/src/__python__/hello.py > \
  $GOPATH/src/__python__/hello/module.go
  
echo 'from hello import hello; hello()' | grumprun
```

```
```


