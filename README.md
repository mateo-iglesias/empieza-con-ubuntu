# 🐧 Empieza en Linux con Ubuntu

> Si vas a dar el salto a Linux, empieza por Ubuntu. Aquí te cuento por qué, desde mi experiencia, y te dejo una guía paso a paso para instalarlo.

![Ubuntu](https://img.shields.io/badge/Ubuntu-26.04_LTS-E95420?logo=ubuntu&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Principiantes-FCC624?logo=linux&logoColor=black)
![Licencia](https://img.shields.io/badge/licencia-MIT-blue)

---

## 📑 Contenido

1. [Por qué escribí esto](#-por-qué-escribí-esto)
2. [Por qué Linux](#-por-qué-linux)
3. [Por qué empezar con Ubuntu](#-por-qué-empezar-con-ubuntu)
4. [Sistema principal vs. máquina virtual](#-sistema-principal-vs-máquina-virtual)
5. [Mi configuración: Windows + Ubuntu](#-mi-configuración-windows--ubuntu)
6. [Guía de instalación de Ubuntu](#-guía-de-instalación-de-ubuntu)
7. [Primeros pasos después de instalar](#-primeros-pasos-después-de-instalar)
8. [Recursos](#-recursos)

---

## 💬 Por qué escribí esto

Muchas personas están acostumbradas a Windows y son reacias a probar otro sistema operativo. Es normal: es lo que usamos desde el colegio, lo que viene en el computador y lo que "todo el mundo usa".

**Yo era así.** Le tenía desconfianza a Linux: pensaba que era complicado, que todo era con comandos y que solo servía para expertos. Eso cambió cuando conocí **Ubuntu**. Hoy trabajo en administración de redes y soporte TI, y Ubuntu es mi herramienta principal para todo lo técnico.

Este repo es lo que me habría gustado leer cuando empecé.

---

## 🐧 Por qué Linux

- **Es libre y gratuito.** Sin licencias, sin activaciones.
- **Es el estándar en tecnología.** La mayoría de servidores, la nube, los routers, los contenedores y las herramientas de ciberseguridad corren sobre Linux. Si trabajas en TI, lo vas a usar sí o sí.
- **La terminal es una ventaja, no un obstáculo.** Instalar, actualizar, automatizar y diagnosticar se hace en segundos.
- **Programas nativos.** Muchas herramientas de redes, programación y seguridad (`nmap`, `wireshark`, `ssh`, `python`, `git`, `docker`…) nacieron en Linux y corren sin trucos ni capas extra.
- **Seguro y estable.** Modelo de permisos sólido, actualizaciones constantes y mucho menos malware dirigido.
- **Ligero y tuyo.** Tú decides qué se instala, qué se ejecuta y cómo se ve.

---

## 🟠 Por qué empezar con Ubuntu

Hay cientos de distribuciones Linux. Para empezar, Ubuntu es la apuesta segura:

| Ventaja | Qué significa para ti |
|---|---|
| **La comunidad más grande** | Casi cualquier error que tengas ya lo resolvió alguien y está en un foro o tutorial. |
| **Versiones LTS** | Soporte y actualizaciones de seguridad por 5 años. Instalas y te olvidas. |
| **Fácil de instalar** | Instalador gráfico, en español, en pocos clics. |
| **Compatible** | Reconoce la mayoría del hardware (Wi‑Fi, video, impresoras) sin configurar nada. |
| **Mucho software** | Tienda de aplicaciones + `apt` + `snap`. Lo que buscas, está. |
| **Lo usa la industria** | Es de los sistemas más usados en servidores y en la nube. Lo que aprendes te sirve en el trabajo. |

### Cosas que son más sencillas en Ubuntu

```bash
# Instalar varios programas de una sola vez
sudo apt install git python3 nmap wireshark htop

# Actualizar TODO el sistema y los programas con un comando
sudo apt update && sudo apt upgrade -y

# Conectarte a un servidor o router por SSH sin instalar nada extra
ssh usuario@192.168.1.1
```

Nada de buscar instaladores `.exe` en páginas raras, ni de reiniciar cada vez que se actualiza algo.

---

## 💻 Sistema principal vs. máquina virtual

Una máquina virtual (VirtualBox, VMware) sirve para **probar**, pero para **aprender y trabajar de verdad** Ubuntu es mucho mejor como sistema principal:

| | Máquina virtual | Sistema principal |
|---|---|---|
| Rendimiento | Comparte RAM y CPU con Windows; se siente lento | Usa todo el hardware |
| Hardware | Acceso limitado a Wi‑Fi, USB, tarjeta de red, GPU | Acceso directo y completo |
| Redes | Adaptadores virtuales, NAT, configuraciones extra | Las interfaces reales del equipo |
| Aprendizaje | Lo abres "cuando toca" | Lo usas todos los días y aprendes más rápido |

Para redes y ciberseguridad esto pesa mucho: capturar tráfico, usar adaptadores USB o trabajar con la interfaz física es más directo sin una capa de virtualización en medio.

---

## 🧩 Mi configuración: Windows + Ubuntu

No se trata de odiar Windows. Cada sistema tiene su lugar:

- 🪟 **Windows** → estudio y cosas personales.
- 🐧 **Ubuntu** → todo lo de tecnología: redes, servidores, scripts, Python, ciberseguridad. Lo llevo incluso en el portátil que uso en campo.

Tener un equipo dedicado a Ubuntu (o un arranque dual) te da lo mejor de los dos mundos.

---

## 🚀 No le tengas miedo

- **No vas a dañar tu computador.** Puedes probar Ubuntu desde una USB *sin instalar nada*.
- **No necesitas saber comandos.** Ubuntu tiene escritorio, tienda de apps y configuración gráfica. La terminal la aprendes poco a poco.
- **Si algo falla, la solución está en internet.** La comunidad es enorme.
- **Lo que aprendas te sirve para tu carrera.** Linux aparece en casi todas las ofertas de TI.

---

## 📀 Guía de instalación de Ubuntu

> Versión recomendada: **Ubuntu Desktop 26.04 LTS** (soportada hasta abril de 2031). Si tu equipo tiene poca RAM, **Ubuntu 24.04 LTS** sigue siendo una gran opción.

### ✅ Requisitos

| Recurso | Ubuntu 26.04 LTS | Ubuntu 24.04 LTS |
|---|---|---|
| Procesador | Doble núcleo, 2 GHz | Doble núcleo, 2 GHz |
| RAM | 6 GB | 4 GB |
| Disco | 25 GB libres | 25 GB libres |

También necesitas:

- Una **memoria USB de 8 GB o más** (se borrará).
- **Conexión a internet** (recomendado).
- **Copia de seguridad** de tus archivos importantes. ⚠️ Siempre.

### 1. Descargar Ubuntu

Entra a 👉 [ubuntu.com/download/desktop](https://ubuntu.com/download/desktop) y descarga la imagen ISO de la versión LTS.

### 2. Crear la USB booteable

Con una de estas herramientas:

- **[balenaEtcher](https://etcher.balena.io/)** (Windows, macOS, Linux) — la más sencilla:
  1. *Flash from file* → elige la ISO.
  2. *Select target* → elige la USB.
  3. *Flash!* y espera.
- **[Rufus](https://rufus.ie/)** (Windows):
  1. Dispositivo → tu USB.
  2. Selección de arranque → la ISO.
  3. Esquema de partición → **GPT** (equipos modernos con UEFI).
  4. *Empezar*.

### 3. Preparar el equipo

- Si vas a **conservar Windows** (arranque dual):
  - Desactiva el **Inicio rápido** de Windows: *Panel de control → Opciones de energía → Elegir el comportamiento de los botones de inicio/apagado → desmarcar "Activar inicio rápido"*.
  - Si tienes **BitLocker** activo, guarda tu clave de recuperación o suspéndelo antes de continuar.
  - Opcional: libera espacio desde *Administración de discos → Reducir volumen* (mínimo 25 GB, ideal 50 GB+).
- **Secure Boot** puede quedarse activado; Ubuntu es compatible.

### 4. Arrancar desde la USB

1. Conecta la USB y reinicia.
2. Presiona la tecla del **menú de arranque** mientras enciende:

| Marca | Tecla habitual |
|---|---|
| HP | `F9` |
| Dell | `F12` |
| Lenovo | `F12` (o botón *Novo*) |
| Asus | `F8` o `Esc` |
| Acer | `F12` |
| MSI | `F11` |

3. Elige la USB → **Try or Install Ubuntu**.

### 5. Probar (opcional) e instalar

1. Selecciona **Español** como idioma.
2. Puedes elegir **Probar Ubuntu** para revisar que Wi‑Fi, sonido y pantalla funcionen *sin tocar tu disco*.
3. Cuando estés listo, abre **Instalar Ubuntu** y sigue el asistente:
   - Distribución del teclado: **Español (Latinoamérica)** o la que uses.
   - Conéctate a internet.
   - Tipo de instalación: **interactiva** y selección **predeterminada** (puedes marcar *software de terceros* para controladores de video y Wi‑Fi y códecs multimedia).

### 6. Elegir cómo instalar

| Opción | Cuándo usarla |
|---|---|
| **Instalar Ubuntu junto a Windows** | Quieres conservar Windows (arranque dual). Al encender eliges cuál usar. |
| **Borrar disco e instalar Ubuntu** | Equipo dedicado solo a Ubuntu. ⚠️ Borra **todo** el disco. |
| **Instalación manual** | Ya sabes de particiones y quieres controlar cada una. |

> 💡 Si tu disco no está cifrado y quieres proteger tus datos, puedes activar el **cifrado de disco** en las opciones avanzadas. Guarda bien la clave.

### 7. Crear tu usuario

- Nombre, nombre del equipo, usuario y **contraseña segura** (la usarás con `sudo`).
- Zona horaria: **America/Bogota** (o la tuya).
- Revisa el resumen → **Instalar** → al terminar, **Reiniciar** y retira la USB.

¡Listo! Ya tienes Ubuntu. 🎉

---

## 🛠️ Primeros pasos después de instalar

```bash
# 1. Actualizar el sistema
sudo apt update && sudo apt upgrade -y

# 2. Herramientas básicas
sudo apt install -y git curl wget htop net-tools build-essential

# 3. Códecs multimedia y fuentes (si no los marcaste al instalar)
sudo apt install -y ubuntu-restricted-extras

# 4. Activar el firewall
sudo ufw enable
sudo ufw status

# 5. Controladores adicionales (video NVIDIA, Wi‑Fi, etc.)
sudo ubuntu-drivers install
```

También revisa:

- **Software y actualizaciones → Controladores adicionales** para drivers propietarios.
- **Centro de aplicaciones** para instalar programas de forma gráfica.
- **Configuración → Energía / Pantalla** para ajustarlo a tu gusto.

### Comandos para empezar a perderle el miedo a la terminal

| Comando | Para qué sirve |
|---|---|
| `pwd` | Ver en qué carpeta estás |
| `ls -la` | Listar archivos (incluidos los ocultos) |
| `cd carpeta` | Entrar a una carpeta |
| `mkdir nueva` | Crear una carpeta |
| `cp` / `mv` / `rm` | Copiar / mover / borrar |
| `sudo` | Ejecutar como administrador |
| `ip a` | Ver tus interfaces y direcciones IP |
| `ping 8.8.8.8` | Probar conexión |
| `man comando` | Ver el manual de cualquier comando |

---

## 📚 Recursos

- [Descargar Ubuntu Desktop](https://ubuntu.com/download/desktop)
- [Tutorial oficial: instalar Ubuntu Desktop](https://ubuntu.com/tutorials/install-ubuntu-desktop)
- [Notas de la versión Ubuntu 26.04 LTS](https://documentation.ubuntu.com/release-notes/26.04/)
- [Ask Ubuntu](https://askubuntu.com/) — preguntas y respuestas
- [Ubuntu Discourse](https://discourse.ubuntu.com/) — foro oficial

---

## 👤 Autor

**Anderson Mateo Iglesias Suárez**
Administración de redes y soporte TI · Estudiante de Ingeniería de Sistemas · ciberseguridad
