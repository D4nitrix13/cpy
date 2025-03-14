<!-- Autor: Daniel Benjamin Perez Morales -->
<!-- GitHub: https://github.com/D4nitrix13 -->
<!-- Gitlab: https://gitlab.com/D4nitrix13 -->
<!-- Correo electrónico: danielperezdev@proton.me  -->
# ***CPY - Implementación del comando cp en Python***

*Este script implementa una versión basica del comando `cp` en Python, que permite copiar ficheros y directorios de manera recursiva si es necesario. Esta implementación es útil cuando el comando `cp` no está disponible o se necesita una funcionalidad personalizada.*

## ***Uso***

*Para ejecutar el script, simplemente llama a `cpy.py` con los siguientes argumentos:*

```bash
python3 cpy.py [-h] [-o] [-i] [-r] [-v] source destination
```

### ***Argumentos***

- *`source`: Directorio o fichero de origen que se copiará.*

- *`destination`: Directorio o fichero de destino donde se copiará `source`.*

#### ***Opciones***

- *`-h`, `--help`: Muestra un mensaje de ayuda y sale.*

- *`-o`, `--override`: Sobrescribe los ficheros de destino si ya existen.*

- *`-i`, `--interactive`: Pregunta si se desea sobrescribir el fichero si ya existe en el destino.*

- *`-r`, `--recursive`: Copia los directorios de forma recursiva.*

- *`-v`, `--verbose`: Proporciona detalles sobre las acciones que se están realizando.*

## ***Ejemplos de Uso***

1. *Copiar un fichero:*

    ```bash
    python3 cpy.py file.txt new_directory/
    ```

2. *Copiar un directorio recursivamente:*

    ```bash
    python3 cpy.py -r directory/ new_directory/
    ```

3. *Copiar un fichero sobrescribiendo el destino si ya existe:*

    ```bash
    python3 cpy.py -o file.txt existing_directory/
    ```

4. *Copiar un fichero interactivo:*

```bash
python3 cpy.py -i file.txt existing_directory/
```

## ***Generación del Binario***

*Para generar el binario de CP, sigue estos pasos:*

### ***Instalación Python, Pip, Pyinstaller en sistemas basados en Apt (Ubuntu, Debian):***

- *Descarga e instala Python desde [Python3](https://www.python.org/downloads/. "https://www.python.org/downloads/.")*

- **Python:**

    ```bash
    sudo apt update
    sudo apt install python3
    ```

- **Instala pip:**

- *Si estás utilizando una versión reciente de Python (a partir de la versión 3.4), pip ya debería estar instalado. De lo contrario, sigue las instrucciones en [pip3](https://pip.pypa.io/en/stable/installation/ "https://pip.pypa.io/en/stable/installation/") para instalar pip.*

- **pip:**

    ```bash
    sudo apt update
    sudo apt install python3-pip
    ```

**Instala PyInstaller:**

- *Ejecuta el siguiente comando en tu terminal para instalar PyInstaller:*

    ```bash
    pip install pyinstaller
    ```

- **PyInstaller:**

    ```bash
    sudo apt update
    sudo apt install pyinstaller
    ```

### ***Instalación Python, Pip, Pyinstaller en sistemas basados en Arch Linux***

- **Python**

```bash
sudo pacman -Syu python
```

- **pip**

```bash
sudo pacman -Syu python-pip
```

- **PyInstaller**

```bash
sudo pacman -Syu pyinstaller
```

- *Estos comandos instalarán Python, pip y PyInstaller en los sistemas correspondientes. Recuerda que es posible que necesites privilegios de superusuario (sudo) para ejecutar estos comandos. Una vez instalados, podrás usar estas herramientas según sea necesario, como se describe en el README.*

**Genera el binario:**

- *Clona el repositorio desde la URL: [repository](https://github.com/D4nitrix13/cpy "https://github.com/D4nitrix13/cpy")*

  - *Navega al directorio **cpy/src** en tu terminal.*

    ```bash
    cd ./src
    ```

  - *Ejecuta el siguiente comando para generar el binario:*

    ```bash
    pyinstaller --onefile ./cpy.py
    ```

  - *Esto creará un fichero ejecutable llamado cp en el directorio cpy/src/dist. Ahora puedes ejecutar el binario de CP en tu sistema Linux.*
  
  ```bash
  user@user-host:~/Desktop/cpy/src/$ tree -C
  .
  ├── build
  │   └── cp
  │       ├── Analysis-00.toc
  │       ├── base_library.zip
  │       ├── cp.pkg
  │       ├── EXE-00.toc
  │       ├── localpycs
  │       │   ├── pyimod01_archive.pyc
  │       │   ├── pyimod02_importers.pyc
  │       │   ├── pyimod03_ctypes.pyc
  │       │   └── struct.pyc
  │       ├── PKG-00.toc
  │       ├── PYZ-00.pyz
  │       ├── PYZ-00.toc
  │       ├── warn-cp.txt
  │       └── xref-cp.html
  ├── cpy.py
  ├── cp.spec
  └── dist
      └── cp

  4 directories, 16 files
  ```

  ```bash
  user@user-host:~/Desktop/cpy/src/$ cd ./dist/
  ```

  ```bash
  user@user-host:~/Desktop/cppy-cli/src/dist$ ./cpy --help
  usage: cpy [-h] [-o | -i] [-r] [-v] source  destination

  cp command implementation in Python

  positional arguments:
  source             Source directory or file
  destination        Destination directory or  file

  options:
  -h, --help         show this help message and  exit
  -o, --override     Override destination files  if they already exist
  -i, --interactive  Asks if you want to  overwrite the file
  -r, --recursive    Copy directories  recursively
  -v, --verbose      Give details about actions  being performed
  ```

## **Contribuciones**

> ¡Se aceptan contribuciones! Si tienes sugerencias, correcciones o deseas agregar contenido adicional a este proyecto, no dudes en abrir un problema o enviar una solicitud de extracción. Tu ayuda es fundamental para hacer de este proyecto una referencia completa y actualizada para la comunidad de desarrollo.

## **Licencia**

> Este repositorio se publica bajo la Licencia MIT. Siéntete libre de utilizar, modificar y distribuir el contenido de acuerdo con los términos de esta licencia.

## ***Autor***

- ***Autor:** Daniel Benjamin Perez Morales*

- ***GitHub:** [D4nitrix13](https://github.com/D4nitrix13 "https://github.com/D4nitrix13")*

- ***Correo electrónico:** <danielperezdev@proton.me>*
