(Unofficial) Python Bindings for the glot.io API.  
https://pypi.org/project/glotio-api/1.0.1/

## Installation

```
$ pip install glotio-api
```

## Basic Usage

```py
from glotio import Runner 


g = Runner("[YOUR_API_KEY]")

# language list
print(Runner.get_lang().keys())

g.set_lang("python")
code = "import sys;print(input() + ', ' + sys.argv[1])"
g.set_code(code, filename="main.py")
g.set_stdin("input text")
g.set_command("python3 main.py 'command line argument'")

result = g.run()
print(result)
```

## LICENCE

glotio-api is made available under an [MIT License](https://github.com/raster0x2a/glotio-api/edit/master/LICENSE).
