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
        <li><a href="#matrix-profiling">Matrix Profiling</a></li>
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

Users of this repo can conduct training and configuring Matrix Profiles through the MPAD framework for detecting anomalies on new time series.

### Framework  

The framework contains two main components: **Matrix Profiling** and **Anomaly Detection**.

The details of the **Matrix Profiling** will be introduced in the subsection below. In short, Matrix Profiles measures the similarity joint between one time series with itself or two time series, in which the similarity joint (i.e., the MP) could be leveraged to identify the similarities and differences. The generated Matrix Profiles can provide a view of the repeated patterns and anomalies across the time series.

For the **Anomaly Detection**, the peak detection algorithm ***g(Ξ)*** may identify multiple peaks due to signal noise and thus generate false positive results. As such, two alternative heuristics methods of preprocessing πππΈπ΅ profile were considered in anomaly detection process. The first one applies a median filter to the matrix profile before peak detection. It is a preprocessing approach when the noise of the πππΈπ΅ is high to an extent that could result in false positive detections. The second method uses an algorithm to find an optimal piecewise linear regression (PWLF) of the πππΈπ΅ using 10 pieces. Although this approach helps identify the trend of the MP, the optimization step results in added computational cost.

Apart from prediction anomalies using single channels, to identify a practical approach in using a set of different channels/inputs for anomaly detection, the MPAD framework also includes combining multiple channels. The multi-channel anomaly detection relies on using kernel density estimation to combine the detected anomalies across different channels into a probability distribution function for collective prediction of anomalies.

<img src="https://github.com/Test1122th/test2/blob/main/imgs/MPAD Framework.png" width="800" height="250" /> 

### Matrix Profiling

The MPAD centers around the Matrix Profile. Figure below shows an example of matrix profile generated by two time series, including a benchmark time series (πππ΅), which does not have any anomalies, and an evaluation time series (πππΈ) that is used to be compared against.

Using a sliding window of size (π€) for subsequence extraction on both benchmark and evaluation time series, a similarity joint for πππΈ with respect to πππ΅ is generated as the πππΈπ΅ matrix profile. On the πππΈπ΅ profile, higher values are associated with subsequences in the πππΈ that do not match with the observations in the πππ΅. This profile is used to identify the location of potential anomalies by running a peak selection algorithm.

<img src="https://github.com/Test1122th/test2/blob/main/imgs/mp_flow.png" width="550" height="620" />

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Getting Started

### Required Environment/Packages

The following main packages were usedοΌ   
[matplotlib](https://matplotlib.org/stable/users/installing/index.html)  / [scikit-learn](https://scikit-learn.org/stable/install.html) / [numpy](https://numpy.org/install/) / [pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html) / [spicy](https://docs.zeek.org/projects/spicy/en/latest/installation.html#) / [pwlf](https://pypi.org/project/pwlf/) / [session-info](https://pypi.org/project/session-info/)  / [cupy](https://docs.cupy.dev/en/stable/install.html) (Optional for users with GPU)

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

[Tianzhi He](https://scholar.google.com/citations?user=0jbujB8AAAAJ&hl=en) - tianzhi@vt.edu
- PhD student at Virginia Tech, Department of Civil and Environmental Engineering, INFORM Lab


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Acknowledgments 

Here are some resources that are helpful to the creation of this Project Repository.

* [Choose an Open Source License](https://choosealicense.com)
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
