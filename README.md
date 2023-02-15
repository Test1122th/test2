<a name="readme-top"></a>


# MPAD

This is the code repository for **MPAD** (**M**atrix **P**rofiling **A**nomaly **D**etection).

Users of this repo can conduct matrix profiling through the MPAD framework for detecting anomalies on new time series. 

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#introduction">Introduction</a>
      <ul>
        <li><a href="#framework">Framework</a></li>
        <li><a href="#matrix-profile">Matrix Profile</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#required-packages">Required Packages</a></li>
        <li><a href="#demo-project">Demo Project</a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>


## Introduction
**MPAD** is a Matrix Profiling-based anomaly detection framework. 

### Framework  

The framework contains two main components: Matrix Profiling and Anomaly Detection.


<img src="https://github.com/Test1122th/test2/blob/main/imgs/MPAD Framework.png" width="800" height="250" /> 

### Matrix Profile

The MPAD centers around the Matrix Profile

<img src="https://github.com/Test1122th/test2/blob/main/imgs/matrix_profile_score.png" width="800" height="140" />

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Getting Started

### Required Environment/Packages

The following main packages were used：   
[matplotlib](https://matplotlib.org/stable/users/installing/index.html)  / [scikit-learn](https://scikit-learn.org/stable/install.html) / [tensorflow](https://www.tensorflow.org/install) / [keras](https://pypi.org/project/keras/) / [numpy](https://numpy.org/install/) / [pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html) / [spicy](https://docs.zeek.org/projects/spicy/en/latest/installation.html#) / [tqdm](https://pypi.org/project/tqdm/) / [session-info](https://pypi.org/project/session-info/) 

All the packages can also be referred in [requirements](requirements.txt).

This file may be used to create an environment using:
```
$ pip install -r requirements.txt
```

  
### Demo Project

[mpad_demo.ipynb](mpad_demo.ipynb) is an example of how to apply the DEGAN framework with your own time series datasets.

To test and use the framework, you may get a local copy and run the example steps in the demo file.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## License

**MIT License**

Copyright (c) 2023 NAME HERE

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Contact

[Farrokh Jazizadeh](https://www.inform-lab.org/farrokh-jazizadeh) - jazizade@vt.edu
- Associate Professor at Virginia Tech, Department of Civil and Environmental Engineering, INFORM Lab

[Yueyan Gu](https://yueyangu.github.io/aboutme/) - yueyangu@vt.edu
- PhD student at Virginia Tech, Department of Civil and Environmental Engineering, INFORM Lab

Tianzhi He - tianzhi@vt.edu
- PhD student at Virginia Tech, Department of Civil and Environmental Engineering, INFORM Lab


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Acknowledgments

Here are some resources that are helpful to the creation of this Project Repository.

* [Choose an Open Source License](https://choosealicense.com)
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
