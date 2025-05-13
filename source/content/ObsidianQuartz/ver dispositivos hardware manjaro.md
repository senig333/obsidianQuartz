<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# ver dispositivos  hardware manjaro

Para ver la información del hardware en Manjaro, tienes varias opciones que incluyen herramientas gráficas y comandos desde la terminal. Aquí te detallo las principales:

## **Herramientas gráficas**

1. **HardInfo**:
    - Es una aplicación que muestra información detallada sobre el hardware y permite realizar benchmarks.
    - Para instalarla, usa el comando:

```bash
sudo pacman -S hardinfo
```

    - Una vez instalada, ejecútala para ver un resumen del hardware y explorar las secciones específicas en su interfaz gráfica[^1][^3].

## **Comandos útiles en la terminal**

Manjaro, como una distribución basada en Arch Linux, permite usar comandos comunes para obtener información detallada del hardware:

1. **`inxi`**:
    - Es una herramienta versátil para obtener datos del sistema. Por ejemplo:
        - Información completa:

```bash
inxi -F
```

        - Información específica (sensores):

```bash
inxi -s
```

    - Si no está instalado, puedes añadirlo con:

```bash
sudo pacman -S inxi
```

2. **`mhwd` (Manjaro Hardware Detection)**:
    - Es específico de Manjaro y útil para gestionar controladores de hardware (especialmente gráficos).

```bash
mhwd -l
```

    - Muestra los controladores disponibles y detecta hardware automáticamente[^6][^8].
3. **Otros comandos generales**:
    - **`lshw`**: Muestra detalles completos del hardware.

```bash
sudo lshw
```

    - **`lspci`**: Lista dispositivos PCI conectados.

```bash
lspci -tv
```

    - **`lsusb`**: Muestra dispositivos USB conectados.

```bash
lsusb -tv
```

    - **`dmidecode`**: Información de la BIOS/UEFI y componentes internos.

```bash
sudo dmidecode -q
```


## **Recomendación**

Para obtener un análisis completo, combina herramientas gráficas como *HardInfo* con comandos avanzados como `inxi`, `mhwd`, `lshw`, y otros según tus necesidades. Esto te permitirá identificar cualquier componente o resolver problemas relacionados con el hardware en tu sistema Manjaro[^1][^5][^6].

<div style="text-align: center">⁂</div>

[^1]: https://hardzone.es/tutoriales/mantenimiento/informacion-hardware-linux/

[^2]: https://www.youtube.com/watch?v=JJM2j315Lhk

[^3]: https://weblinus.com/como-ver-info-del-sistema-y-hardware-instalado-en-linux/

[^4]: https://laguialinux.es/comandos-para-obtener-informacion-de-nuestro-sistema-linux-y-su-hardware/

[^5]: https://www.youtube.com/watch?v=6aDkbVgtSAA

[^6]: https://wiki.manjaro.org/index.php/Manjaro_Hardware_Detection

[^7]: https://www.profesionalreview.com/2018/04/01/como-verificar-la-informacion-sobre-el-hardware-en-linux/

[^8]: https://wiki.manjaro.org/index.php/Manjaro_Hardware_Detection_Overview

