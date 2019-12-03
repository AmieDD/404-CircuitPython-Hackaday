# 404 CircuitPython Hack
404 CircuitPython PyBadge hack for my 2019 Hackaday SuperCon badge

```python
from adafruit_pybadger import PyBadger

pybadger = PyBadger()

pybadger.auto_dim_display(delay=30)

first_display = True

while True:
    pybadger.pixels[0] = (227,0,11)
    pybadger.pixels[1] = (255,10,10)
    pybadger.pixels[2] = (255,20,10)
    pybadger.pixels[3] = (255,30,10)
    pybadger.pixels[4] = (255,40,10)

    if pybadger.button.a:
        pybadger.show_business_card(image_name="supercon.bmp", name_string="Amie DD", name_scale=1,
                                    email_string_one="amie@amiedd.com",
                                    email_string_two="https://amiedd.com")
    elif pybadger.button.b:
        pybadger.show_qr_code(data="https://www.amiedd.com")
    elif pybadger.button.start or first_display:
        pybadger.show_badge(name_string="Amie DD", hello_scale=2, my_name_is_scale=2, name_scale=2)
        first_display = False
        
```

## Hardware
[Adafruit PyBadge for CircuitPython](https://www.adafruit.com/product/4200)
