# Installation

## Compatibility
* Windows 10 Pro
* Windows 11 Pro
* Mac OS  - Apple Silicon M1, M2
* Mac OS  - Intel Chip i5

## Requirements - Windows and MacOS users
* [Anaconda 3](https://www.anaconda.com/distribution/) : Python package manager
* [Docker Desktop](https://www.docker.com/products/docker-desktop) : Virtualization environment
* [Rhino 7 & Grasshopper](https://www.rhino3d.com/download) : 3D and parametric modelling software
* [Visual Studio Code](https://code.visualstudio.com/) : Code editor + extensions
  * [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
  * [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)
  * [EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

## Requirements - Windows users only
* [ABB RobotStudio](https://new.abb.com/products/robotics/robotstudio): Robot simulation
* VPN Client

## Requirements - MacOS users only
* [UTM](https://mac.getutm.app) - Virtual Machine for mac


## Instructions 

### Anaconda 3 

1) Download this repository and move it to the Documents folder.

2) Open Anaconda Prompt (Windows) or Terminal (MacOS).

3) Change directory to downloaded repository.
```conda
(base) cd C:\Users\marco\Documents\DP-WS2024-main
```
4) Create environment
```conda
(base) conda env create -f environment.yml
```

5) Add to Rhino
```conda
(base) conda activate dp2024
(dp2024) python -m compas_rhino.install -v 7.0
```

6) Verify installation

```conda
(dp2024) python -m compas

Yay! COMPAS is installed correctly!

COMPAS: 1.17.5
Python: 3.10.9 (CPython)
Extensions: ['compas-occ', 'compas-cgal', 'compas-fab', 'compas-rrc']
```

---
### Rhino 7

1) Type `_EditPythonScript` in the Rhino command line

2) Verify procedure by running the following code in the Python Editor

```python
import compas_fab
print(compas_fab)
```

The code shoud output the following:
```python
<module 'compas_fab' from 'C:\Users\marco\AppData\Roaming\McNeel\Rhinoceros\7.0\scripts\compas_fab\__init__.py'>
```
---

### ABB Robot Studio - Windows users only
* In this repository, go to the folder named `robotstudio`

* Unpack the file `GoFa12_Kunst2.rspag` with a double-click.
* Follow the installation wizard, making sure that:
    * RobotWare Version is `7.15.2`
    * Wizard Easy Programming version is `1.6.0`
* Navigate to the `Controller` tab, open `FlexPendant` and follow installation wizard
---

### UTM - MacOS users only
Add instructions

---

### Docker

* Open Docker Desktop (a Docker icon should appear in the Windows tray)

* Open VS Code and open this repository folder

* Navigate to the `docker\virtual_controller` folder

* Compose up the `docker-compose.yml` file with a right-click








