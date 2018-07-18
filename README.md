# OpenCL Caffe Targeting AMD GPU's OpenCL (Modified to work with MSVC 2017 15.0 and Python 2.7.15) on Windows 10:

**This is an experimental but working repo i.e. forked from official caffe's Opencl branch for targeting AMD GPUs Only. Forked from https://github.com/BVLC/caffe/commit/74312cfc64c07b69616c8d0d5e1b6b020670c783**

## Custom requirements for this branch:

- Git Windows (Intalled and configured)
- Microsoft Visuals 15.0 2017 installed and configured (as compiler).
- Python 2.7.15 installed and configured (for building pycaffe)
- Numpy (`pip install numpy`)
- OpenCV installed (Latest will be good)
- AMD GPU with Latest drivers installed properly
- AMD APP SDK Windows(any version - Preferred-3.0) installed
- ViennaCL Library (Latest version - do not compile or install) as backend.
- AMD GPU ofcourse.

## Configuring and compiling procedure:
Open Command Prompt and follow up:
- `git clone https://github.com/abhiTronix/caffe-opencl-windows-amd.git`
- `cd caffe`
- `git checkout opencl-windows-amd`
- `mkdir build && cd build`
- `cmake -G"Visual Studio 15 2017 Win64" -DBLAS=Open -DViennaCL_INCLUDE_DIR=<path to ViennaCL Library> -DOpenCV_DIR=<path to OpenCV build> -DOPENCL_LIBRARIES= <path to AMD APP SDK Static Library> ..`
- `cmake --build . --target install --config release`

Final Files can be found here: `caffe/build/install`


## Other Custom distributions

- [Intel Caffe](https://github.com/BVLC/caffe/tree/intel) (Optimized for CPU and support for multi-node), in particular Xeon processors (HSW, BDW, Xeon Phi).
- [OpenCL Caffe](https://github.com/BVLC/caffe/tree/opencl) e.g. for AMD or Intel devices.
- [Windows Caffe](https://github.com/BVLC/caffe/tree/windows)

## Community

[![Join the chat at https://gitter.im/BVLC/caffe](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/BVLC/caffe?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Caffe is a deep learning framework made with expression, speed, and modularity in mind.
It is developed by Berkeley AI Research ([BAIR](http://bair.berkeley.edu))/The Berkeley Vision and Learning Center (BVLC) and community contributors.

Caffe is released under the [BSD 2-Clause license](https://github.com/BVLC/caffe/blob/master/LICENSE).
The BAIR/BVLC reference models are released for unrestricted use.
