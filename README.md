<div align="center">
    <h1>MapClosures</h1>
    <a href="https://github.com/PRBonn/MapClosures/releases"><img src="https://img.shields.io/github/v/release/PRBonn/MapClosures?label=version" /></a>
    <a href="https://github.com/PRBonn/MapClosures/blob/main/LICENSE"><img src=https://img.shields.io/badge/license-MIT-green" /></a>
    <a href="https://github.com/PRBonn/MapClosures/blob/main/"><img src="https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black" /></a>
    <a href="https://github.com/PRBonn/MapClosures/blob/main/"><img src="https://img.shields.io/badge/Windows-0078D6?st&logo=windows&logoColor=white" /></a>
    <a href="https://github.com/PRBonn/MapClosures/blob/main/"><img src="https://img.shields.io/badge/mac%20os-000000?&logo=apple&logoColor=white" /></a>
    <br />
    <br />
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://github.com/PRBonn/MapClosures/blob/main/README.md#Install">Install</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href=https://www.ipb.uni-bonn.de/pdfs/gupta2024icra.pdf>ICRA24 Paper</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href=https://github.com/PRBonn/MapClosures/issues>Contact Us</a>
  <br />
  <br />

Effectively Detecting Loop Closures using Point Cloud Density Maps.

<p align="center">

![image](https://github.com/PRBonn/MapClosures/assets/28734882/18d5ee54-61a9-4d9f-87f2-8aba16de0f75)
</p>
</div>
<hr />

## Use MapClosures in your C++ project

1. Include the following snippet in your project's `CMakeLists.txt`:
```cmake
set(USE_SYSTEM_EIGEN3 ON CACHE BOOL "use system eigen3")
set(USE_SYSTEM_OPENCV ON CACHE BOOL "use system opencv")

include(FetchContent)
FetchContent_Declare(
    map_closures
        GIT_REPOSITORY https://github.com/PRBonn/MapClosures.git
        GIT_TAG main
        SOURCE_SUBDIR cpp
)
FetchContent_MakeAvailable(map_closures)

```
You can trigger the automatic installation of the dependencies by playing around with the options in the first three lines of the snippet.

2. Link **MapClosures** against your library or executable:
```cmake
target_link_libraries(my_target PUBLIC map_closures)
```
3. The following _include_ directive in your source code file will provide access to the core API of MapClosures:
```cpp
#include <map_closures/MapClosures.hpp>
```

## Install the Python API and CLI
`pip install map-closures`

### Usage
<details>
<summary>
The following command will provide details about how to use our pipeline:

```sh
map_closure_pipeline --help
```
</summary>

![CLI_usage](https://github.com/PRBonn/MapClosures/assets/28734882/6dfbd767-ca63-4671-9582-3129752d0244)
</details>

<details>
<summary>
Providing the -v flag will initialize the visualizer:

```sh
map_closure_pipeline -v
```
</summary>

![Visualizer](https://github.com/user-attachments/assets/34aa2b2f-c0ce-4dfb-a0e0-cbcc04487a5a)
</details>

## Citation

If you use this library for any academic work, please cite our original [paper](https://www.ipb.uni-bonn.de/pdfs/gupta2024icra.pdf).

```bibtex
@inproceedings{gupta2024icra,
    author     = {S. Gupta and T. Guadagnino and B. Mersch and I. Vizzo and C. Stachniss},
    title      = {{Effectively Detecting Loop Closures using Point Cloud Density Maps}},
    booktitle  = {IEEE International Conference on Robotics and Automation (ICRA)},
    year       = {2024},
    codeurl    = {https://github.com/PRBonn/MapClosures},
}
```
### Paper Results
As we decided to continue the development of **MapClosures** beyond the scope of the ICRA paper, we created a ``git tag`` so that researchers can consistently reproduce the results of the publication. To checkout at this tag, you can run the following:
```sh
git checkout ICRA2024
```
Our development aims to push the performances of **MapClosures** above the original results of the paper.


## Acknowledgement

This repository is heavily inspired by, and also depends on [KISS-ICP](https://github.com/PRBonn/kiss-icp)

## Contributors

<a href="https://github.com/PRBonn/MapClosures/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=PRBonn/MapClosures" />
</a>
