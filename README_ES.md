# 🌙  xsct_tk

[![Topic](https://img.shields.io/badge/topic-linux%20x11%20gui-blueviolet)](https://github.com/topics/linux)

[READ IN ENGLISH](README.md)

## 🌙  xsct_tk – Fácil control de la luz de tu pantalla, para X11 Window Manager

Este programa te ayuda a **ajustar el color y el brillo de tu pantalla** en Linux, para que sea más cómoda de ver, especialmente por la noche.

Es como agregar un "filtro de luz cálida" (similar al modo nocturno de tu teléfono que reduce la luz azul) para reducir la fatiga visual y hacer que el uso de pantallas a altas horas de la noche sea más llevadero para tus ojos.

`xsct_tk` es una **interfaz gráfica** para [xsct](https://github.com/faf0/sct), una pequeña herramienta de línea de comandos que cambia la temperatura de color de la pantalla usando `xrandr`.

---

## 🎯 ¿Qué hace este programa?

- 🔆 **Ajusta el color de la pantalla**: Puedes hacerla más naranja (cálida) o más blanca (fría).
- 💡 **Controla el brillo**: Puedes hacerla más oscura o más clara.
- 🖱️ Todo con una **interfaz sencilla y fácil de usar**, con barras deslizantes.

✅ Ideal para usar de noche, estudiando o trabajando en la computadora.  
💡 Trata de que el color de la pantalla se asemeje al de tu cuarto, y evita luces con mucha luz azul por la noche.

---

## El Sistema Operativo que necesitas

Necesitarás un sistema Linux con el **Gestor de Ventanas X11** (no Wayland).  
A partir de 2025, estos entornos de escritorio aún admiten sesiones X11:

- GNOME
- KDE
- Linux Mint
- XFCE
- LXQt
- LXDE
- openbox, fluxbox, jwm y otros gestores de ventanas X11

> ❗ Esta herramienta **no funciona en Wayland**. Asegúrate de iniciar sesión con una sesión X11.

### Software requerido

Antes de usar `xsct_tk`, asegúrate de tener estos instalados (abre una terminal y ejecuta):

```bash
sudo apt install python3 python3-tk xsct python3-pil.imagetk python3-cairosvg papirus-icon-theme
```

La siguiente es una tabla con la descripción de cada uno:

|              Programa              |                       ¿Para qué sirve?                       |
| ---------------------------------- | ------------------------------------------------------------ |
| **Python 3**                       | El lenguaje de programación en el que está hecho el programa.|
| **Tkinter** (`python3-tk`)         | Crea la ventana y los botones (kit de herramientas GUI).     |
| **Pillow** (`python3-pil.imagetk`) | Muestra las barras de degradado de colores.                  |
| **CairoSVG** (`python3-cairosvg`)  | Permite mostrar íconos SVG (como el ícono de la aplicación). |
| **xsct**                           | La herramienta que realmente cambia el color de tu pantalla. |
| **Papirus Icon Theme**             | Proporciona un ícono bonito a la ventana.                    |

> 📝 Si usas **Debian 11 (bullseye)** o **Debian 10 (buster)**, `xsct` no está disponible. Deberás compilarlo manualmente (ver instrucciones al final).

---

## 🐧 Soporte de distribuciones Linux

### Ubuntu (y sabores como Kubuntu, Xubuntu, etc.)
Si usas Ubuntu y sus sabores que admiten inicio de sesión con X11, esos paquetes están disponibles en los repositorios:

- [https://packages.ubuntu.com/xsct](https://packages.ubuntu.com/xsct) **Desde Noble (24.04LTS)**
- [https://packages.ubuntu.com/papirus-icon-theme](https://packages.ubuntu.com/papirus-icon-theme) Desde Jammy (22.04LTS)
- [https://packages.ubuntu.com/python3](https://packages.ubuntu.com/python3) Desde Jammy (22.04LTS)
- [https://packages.ubuntu.com/python3-tk](https://packages.ubuntu.com/python3-tk) Desde Jammy (22.04LTS)
- [https://packages.ubuntu.com/python3-pil.imagetk](https://packages.ubuntu.com/python3-pil.imagetk) Desde jammy (22.04LTS)
- [https://packages.ubuntu.com/python3-cairosvg](https://packages.ubuntu.com/python3-cairosvg) Desde jammy (22.04LTS)

📌 **Nota:** Linux Mint está basado en Ubuntu, por lo que estos paquetes pueden tener los mismos nombres allí.

### Debian (y derivados como MX Linux, antiX)
Si usas Debian y sus derivados como MX Linux, antiX, etc., donde puedes iniciar sesión con X11, esos paquetes están disponibles en los repositorios:

* [https://packages.debian.org/xsct](https://packages.debian.org/xsct) **desde Debian 12**
* [https://packages.debian.org/papirus-icon-theme](https://packages.debian.org/papirus-icon-theme) desde Debian 10
* [https://packages.debian.org/python3](https://packages.debian.org/python3) desde Debian 10
* [https://packages.debian.org/python3-tk](https://packages.debian.org/python3-tk) desde Debian 10
* [https://packages.debian.org/python3-pil.imagetk](https://packages.debian.org/python3-pil.imagetk) Desde Debian 10
* [https://packages.debian.org/python3-cairosvg](https://packages.debian.org/python3-cairosvg) Desde Debian 10

📌 **Nota:** MX Linux 23, antiX 23 y otros están basados en Debian 12

---

## ▶️ Cómo usar el programa
Lo primero es tener el programa en una carpeta en tu ordenador con Linux

### **1era OPCIÓN: Descargar el repositorio**
Ve al sitio web:

[https://github.com/wachin/xsct_tk](https://github.com/wachin/xsct_tk)

haz clic en la especie de flecha desplegable en Code:

**<>  Code ▼**

y haz clic en:

**Download ZIP**

descomprímelo, y dentro de la carpeta encontrarás el archivo `Launcher.sh`
o puedes clonarlo:

### **2da OPCIÓN: Clonar el repositorio**

**1.-** Como ya tenemos git instalado, abre una terminal en una carpeta donde tengas programas de Linux:

```bash
git clone https://github.com/wachin/xsct_tk  
```

y entra allí con:

```bash
cd xsct_tk  
```

## Ejecutar

ejecuta con:

```bash
python3 xsct_tk.py  
```

## Ejecutar con el lanzador

Alternativamente, ejecuta con el lanzador: asegúrate de que el script `Launcher.sh` sea ejecutable. En el administrador de archivos, haz clic derecho y en la pestaña "**Permisos**" asegúrate de que "**es ejecutable**".
Haz doble clic en el script `Launcher.sh` y haz clic en `Ejecutar`.

👉 Se abrirá una ventana con dos controles:

![](https://blogger.googleusercontent.com/img/a/AVvXsEixMsvdzTpTY5ENvil5n1a9KoIlz3rWyYkq1qlxnS4OPN_47wJmk5uBqhvM1PZu0fhNqgRf8_ttnMRlyjxns5iyFEBqZ8CIiLk22lq6Ak86gAa0O9tOxqeIrjOOQKI1WHKq4JS-2_5tvUZPZNWLCeNrnDjh-9xw2fvz54a56Rvnc9R_59TVd8EEWi7aLdc=s16000-rw)

# Ejecutar con el lanzador de Python

En algunos Linux como MX Linux puedes hacer clic derecho en el archivo `xsct_tk.py` y abrirlo con el lanzador de Python.

---

## 🎛️ Controles de la interfaz

### 1. 🌡️ Temperatura de color (de 2000K a 6500K)
- **Izquierda (2000K)**: tono naranja cálido → ideal para la noche.
- **Derecha (6500K)**: tono blanco frío → ideal para el día.

📌 Mueve el deslizador para elegir el color que prefieras.

### 2. 💡 Brillo (de 0.300 a 1.000)
- **Izquierda (0.300)**: muy oscuro → ideal para habitaciones oscuras.
- **Derecha (1.000)**: brillo máximo → ideal para ambientes luminosos.

📌 Ajusta el deslizador para establecer el brillo deseado.

---

## 🔁 ¿Los cambios se aplican automáticamente?

✅ **¡Sí!** En cuanto mueves un deslizador, el cambio se aplica de inmediato.

También puedes hacer clic en el botón **"Acerca de..."** para ver información sobre el programa.

---

## 💡 Consejos para mejores resultados

|           Situación           |                  Configuración recomendada                  |
| ----------------------------- | ------------------------------------------------------------ |
| 🌙 **De noche o en habitación oscura** | Temperatura 3000K – 4000K, brillo 0.700 – 0.800   |
| ☀️ **Durante el día o con luz natural** | Temperatura 5500K – 6500K, brillo 1.000           |
| 👀 **Ojos cansados**          | Prueba con color más cálido y menos brillo                   |

🔍 **¡Experimenta!** Encuentra la combinación que mejor se adapte a tus ojos y a la iluminación de tu cuarto.

---

## 🛠️ ¿Puedo modificar el programa?

¡Claro! El programa está escrito en **Python**, así que puedes abrir `xsct_tk.py` en cualquier editor de texto (como **Geany**, **Thonny** o **Mousepad**) para:
- Cambiar colores
- Editar etiquetas
- Agregar nuevas funciones

📚 ¡Ideal para aprender **programación de interfaces gráficas con Tkinter** en Python!

---

## 📚 Más información

- 🐍 **Código fuente de la GUI**: [https://github.com/wachin/xsct_tk](https://github.com/wachin/xsct_tk)
- ⚙️ **xsct (herramienta de línea de comandos)**: [https://github.com/faf0/sct](https://github.com/faf0/sct)

---

## 🙌 Sobre este programa

Creado por **Washington Indacochea Delgado**
Licencia: **GNU GPL3** (libre y de código abierto)

✨ ¡Gracias por usar `xsct_tk`!  
Que tu pantalla siempre sea cómoda para tus ojos. 👀💙

---

## 📝 Notas

- En **versiones antiguas de Debian** (como Buster o Bullseye), `xsct` no está disponible. Deberás compilarlo manualmente:

```bash
# Instalar dependencias de compilación
sudo apt install libx11-dev libxrandr-dev

# Clonar y compilar xsct
git clone https://github.com/faf0/sct
cd sct
make
sudo make install
```

Luego instala las dependencias de la GUI:
```bash
sudo apt install python3 python3-tk python3-pil.imagetk python3-cairosvg
```

Ahora ejecuta:
```bash
python3 xsct_tk.py
```

---

✅ ¡Todo listo!  
Ahora prueba cambiar el color de tu pantalla, ¡especialmente de noche! 🌈🖥️  
¡Disfruta de una experiencia informática más cómoda!

> 🙏 Dios les bendiga.
