1) Download this repository and move it to the Documents folder

2) Open Anaconda Prompt (Windows) or Terminal (MacOS)

3) Change directory to downloaded repository
```conda
(base) cd Documents\DP-WS2024-main
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