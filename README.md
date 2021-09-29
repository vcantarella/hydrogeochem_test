
## Introduction

WQChartPy is an an open-source Python package for producing most of the graphical diagrams for visualization of water geochemistry data. Utilizing the commonly used comma-separated values (CSV) file as the input data format, WQChartPy can produce eleven geochemical diagrams including not only the traditional Piper trilinear, Durov, Chadha, Stiff, Chernoff face, Schoeller, Gibbs, and Gaillardet diagram, but also the recently proposed diagrams such as the rectangle Piper, color-coded Piper and HFE-D diagrams that have not been implemented in previous software. 

This is the first release of WQChartPy. As a Python-based cross platform program, WQChartPy works on Windows, MacOS X and GNU/Linux. We provided a self-contained Jupyter notebook file to illustrate how to use WQChartPy. Users with a little Python experience can do the whole process from data to the graphical diagrams. Buidling on the oldest and most popular Python plotting library Matplotlib, the figures generated by WQChartPy can be saved as portable network graphics (PNG), scalable vector graphics (SVG) or portable document format (PDF). WQChartPy is an open-source project and any assistance is welcomed. Please email the development team if you want to contribute.

The repository contains:

```bash
+-- data                                         
¦ +-- data_template.csv                      # Example water geochemsitry dataset
+-- examples         
¦ +-- example1.ipynb                        # Example workflow to illustrate how to use WQChartPy
+-- papers
¦ +-- Chadha-1999-A proposed ...             # Reference for Chadha diagram    
¦ +-- ...                                    # ... 
¦ +-- Ray-2008-Reproducing the ...           # Reference for rectangle Piper diagram    
+-- wqchartpy
¦ +-- __init__.py                            # Common script used in the regular package  
¦ +-- chadha.py                              # Code for generating the Chadha diagram
¦ +-- chernoff.py                            # Code for generating Chernoff faces
¦ +-- color_piper.py                         # Code for generating color-coded Piper diagram
¦ +-- durvo.py                               # Code for generating Durvo diagram
¦ +-- gaillardet.py                          # Code for generating Gaillardet diagram
¦ +-- gibss.py                               # Code for generating Gibbs diagram
¦ +-- hfed.py                                # Code for generating HFE-D diagram
¦ +-- ions.py                                # Code for defining the ion weights and charges
¦ +-- rectangle_piper.py                     # Code for generating rectangle diagram
¦ +-- schoeller.py                           # Code for generating Schoeller diagram
¦ +-- stiff.py                               # Code for generating Stiff diagram
¦ +-- triangle_piper.py                      # Code for generating triangle Piper diagram
+-- LICENCE     
+-- README.md         
+-- setup.py                                 # Centre script of and installing this package
```

## Installation

WQChartPy requires **Python** 3.7 (or higher). We recommend using [Anaconda](https://www.anaconda.com/) on Windows or Linux platforms. 

The easiest way to install is via `pip`:

To install WQChartPy type:

    pip install wqchartpy

To update WQChartPy type:

    pip install wqchartpy --upgrade

To uninstall WQChartPy type:

    pip uninstall wqchartpy
    
Another way is to manually install WQChartPy with `setup.py`. Preliminary steps to take:

    1. Download the package and extract it into a local directory

    2. cd into the root directory where setup.py is located using an Anaconda Prompt

    3. Enter: python setup.py install
    
## Requirements:

- [NumPy](https://www.numpy.org)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://www.scipy.org/scipylib)
- [SciPy](https://salib.readthedocs.io/en/latest/)
    
## How to use

We recommend to start by executing the [workflow](https://github.com/jyangfsu/WQChartPy/blob/main/examples/example1.ipynb) provided in the examples folder. 

| Diagram | Basic usage
---------|------------
Triangle Piper| from wqchartpy import triangle_piper; triangle_piper.plot(df, unit, figname, figformat)
Rectangle Piper| from wqchartpy import rectangle_piper; rectangle_piper.plot(df, unit, figname, figformat)
Color-coded Piper| from wqchartpy import color_piper; color_piper.plot(df, unit, figname, figformat)
Durov| from wqchartpy import durvo; durvo.plot(df, unit, figname, figformat)
Chadha| from wqchartpy import chadha; chadha.plot(df, unit, figname, figformat)
Stiff| from wqchartpy import stiff; stiff.plot(df, unit, figname, figformat)
Chernoff face| from wqchartpy import chernoff; chernoff.plot(df, unit, figname, figformat)
Schoeller| from wqchartpy import schoeller; schoeller.plot(df, unit, figname, figformat)
Gibbs| from wqchartpy import gibbs; gibbs.plot(df, unit, figname, figformat)
Gaillardet| from wqchartpy import gaillardet; gaillardet.plot(df, unit, figname, figformat)
HFE-D| from wqchartpy import hfed; hfed.plot(df, unit, figname, figformat)

### Triangle Piper
![](/examples/triangle Piper diagram.png)


## License

WQChartPy is distributed under the GNU General Public License v3.0. See the [LICENSE](https://github.com/jyangfsu/WQChartPy/LICENSE) file for details.

## Contributing to WQChartPy

Users are welcome to submit bug reports, feature requests, and code contributions to this project through GitHub or mail to us at jingyang@cug.edu.cn or mye@fsu.edu.
