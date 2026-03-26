# Datos

**Nombre:Pineda Gomez Ricardo Alejandro**  
**Matrícula:23212044**  
**Fecha: 26/03/2026**  

---

## Experiencia con micro:bit

Dentro de la experiencia que llegamos a tener con micro:bit, se logró utilizar para la reproducción de música, como dispositivo de grabación y como radio para el envío y recepción de mensajes.

Al final de toda esta experiencia se logró tener un mayor entendimiento respecto al funcionamiento del micro:bit y sus posibles aplicaciones, con una sintaxis simple que da pie a un sin fin de posibilidades respecto a su uso.

---

## Ejemplo de código (Radio)

A continuación dejamos un pequeño ejemplo de uno de los códigos utilizados en las prácticas ya mencionadas, concretamente el código de la radio:

### Receptor

```python
from microbit import *
import radio

radio.config(group=20, power=5)
radio.on()

while True:
    message = radio.receive()
    if message:
        display.scroll(message)
```
### Emisor
```python
from microbit import *
import radio

radio.config(group=20, power=5)
radio.on()

while True:
    if button_a.was_pressed() or button_b.was_pressed():
        radio.send('hello')
