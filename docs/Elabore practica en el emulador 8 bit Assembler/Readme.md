<img width="1761" height="1281" alt="Screenshot 2026-02-26 212336" src="https://github.com/user-attachments/assets/573bc5eb-4a13-49e9-9b07-7b40c3031a6c" />
<img width="3039" height="1517" alt="Screenshot 2026-02-26 211156" src="https://github.com/user-attachments/assets/4576e1e2-5ff0-4988-91e1-f3869c3dfe7e" />
<img width="2100" height="1506" alt="Screenshot 2026-02-26 211140" src="https://github.com/user-attachments/assets/849b7703-1f61-43e9-9501-2a65db0242ee" />
<img width="2121" height="1565" alt="Screenshot 2026-02-26 215345" src="https://github.com/user-attachments/assets/e9e127bd-a3cc-4cf2-ae23-bfe2c5cd49e7" />

.done:
    mov Rb, Rc      ; Rb = 255
    mov Rc, Rb      ; Rc = 255
    inc Rc          ; Rc = 255+1 = 0 (overflow, Rc = 0)
    inc Rc
    inc Rc
    inc Rc
    inc Rc
    inc Rc
    inc Rc
    inc Rc
    inc Rc
    inc Rc
    inc Rc          ; Rc = 10

.loop:
    mov Rd, Rc
    add Rc, Rb      ; Rc - 1
    jc .loop
    mov Rd, Rc
    jmp .done       ; volver a 10 sin reconstruir Rb

Se logró una comprensión de cómo fluye la información a través del bus y de cómo funcionan los saltos condicionales.

Esta práctica permitió comprender de manera clara cómo un programa en ensamblador interactúa directamente con la arquitectura física de una computadora de 8 bits.

La práctica refuerza la comprensión de arquitectura básica de CPU, control por microinstrucciones y flujo condicional en bajo nivel, consolidando la relación directa entre código ensamblador y comportamiento físico del hardware.
