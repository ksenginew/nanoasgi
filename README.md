# NanoASGI
Asynchronous Python Web Framework

---

NanoASGI is a fast:zap:, simple and light:bulb:weight ASGI micro:microscope: web:earth_asia:-framework for Python:snake:. It is distributed as a single file module and has no dependencies other than the Python Standard Library.

## Download and Install
Download :arrow_down: nanoasgi.py into your project directory. There are no hard dependencies other than the Python standard library. NanoASGI runs with Python versions above 3.7.

Or install via pip
```css
pip install NanoASGI
```

## Example
```py
# example.py
from nanoasgi import App, Response

app = App()

@app.on('startup')
async def on_startup():
    print('Ready to serve requests')

@app.on('shutdown')
async def on_shutdown():
    print('Shutting down')

@app.route('GET', '/api/hello/{name}/')
async def hello_handler(request, name):
    return Response(
        {'result': f'Hello {name}!'},
        status=200,
        headers=[('Content-Type', 'application/json')],
    )
```
Then run your app with your favourite ASGI server.
```css
uvicorn example:app
```
## Status
[![GitHub license](https://img.shields.io/github/license/ksenginew/nanoasgi?style=flat-square)](https://github.com/ksenginew/nanoasgi/blob/main/LICENSE)
![PyPI](https://img.shields.io/pypi/v/nanoasgi?logo=pypi&style=flat-square)
![PyPI - License](https://img.shields.io/pypi/l/nanoasgi?style=flat-square)
![PyPI - Status](https://img.shields.io/pypi/status/nanoasgi?style=flat-square)
![PyPI - Format](https://img.shields.io/pypi/format/nanoasgi?style=flat-square)
![PyPI - Downloads](https://img.shields.io/pypi/dm/nanoasgi?style=flat-square)
![PyPI - Wheel](https://img.shields.io/pypi/wheel/nanoasgi?style=flat-square)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/nanoasgi?style=flat-square)


## License
Code and documentation are available according to the MIT License:page_with_curl: (see [LICENSE](https://github.com/ksenginew/nanoasgi)).

