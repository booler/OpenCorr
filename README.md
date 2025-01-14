# OpenCorr
OpenCorr is an open source C++ library for development of 2D, 3D/stereo, and volumetric digital image correlation. It aims to provide a developer-friendly, lightweight, and efficient kit to the users who are willing to study the state-of-the-art DIC/DVC algorithms or to create DIC/DVC programs for their specific applications.

Both the library and the webpage are under construction. Update will be frequent in the following months until we reach a stable version with relatively complete documentation. Comments and sugestions are welcome.

# Get started

OpenCorr is developed and tested in Microsoft Visual Studio on Windows 10. The codes follow the standard of ISO C++ 14, theoretically it can be compiled on other OS like Linux. The building environment requires the following libraries correctly configured:

- Eigen 3.3.9 ([eigen.tuxfamily.org](eigen.tuxfamily.org)), used for basic operations of matrix.
- OpenCV 3.4.5 ([opencv.org](opencv.org)), used to read images, and in modules related with image features and stereovision.
- FFTW 3.3.9 ([fftw.org](fftw.org)), used for cross correlation.

These libraries could be installed by downloading the source files (e.g., .h or .cpp) and static library files (.lib), and then place them into proper directories in your computer. Accordingly, the paths of source files and static library files need to be set in integrated development environment. Figure 1 gives an example in Visual Studio 2019 community version.
![image](https://github.com/vincentjzy/OpenCorr/blob/main/img/configuration_of_path_in_vs.png)
*Figure 1. Illustration of setting paths in Visual Studio 2019*

At last, the dynamic link library files (.dll) need to be placed in the directory where you build the executable programs or the directoris listed in system PATH.

There are some examples in folder "samples", which demonstrate how we use the modules in OpenCorr to build our own DIC programs. The DIC algorithms provided in this library include:

- Fast Fourier transform-based cross correlation (FFT-CC): Estimation of integer-pixel displacement.
- SIFT-aided DIC: Estimation of 1st order deformation
- Inverse compositional Gaussian-Newton (ICGN) algorithm: high accuracy estimation of deformation. Two versions are implemented, one for the 1st order shape function and the other for the 2nd order shape function.

Figure 2 shows the framework of OpenCorr, which gives a guide to understand the structure of OpenCorr.
![image](https://github.com/vincentjzy/OpenCorr/blob/main/img/framework.png)
*Figure 2. Framework of OpenCorr*

# References
Users may refer to our papers for the details of the principle of the algorithms provided in OpenCorr.

[1] Z. Jiang, Q. Kemao, H. Miao, J. Yang, L. Tang, Path-independent digital image correlation with high accuracy, speed and robustness, Optics and Lasers in Engineering, 65 (2015) 93-102.

[2] L. Zhang, T. Wang, Z. Jiang, Q. Kemao, Y. Liu, Z. Liu, L. Tang, S. Dong, High accuracy digital image correlation powered by GPU-based parallel computing, Optics and Lasers in Engineering, 69 (2015) 7-12.

[3] T. Wang, Z. Jiang, Q. Kemao, F. Lin, S.H. Soon, GPU accelerated digital volume correlation, Experimental Mechanics, 56 (2016) 297-309.

[4] W. Chen, Z. Jiang, L. Tang, Y. Liu, Z. Liu, Equal noise resistance of two mainstream iterative sub-pixel registration algorithms in digital image correlation, Experimental Mechanics, 57 (2017) 979-996.

[5] J. Huang, L. Zhang, Z. Jiang, S. Dong, W. Chen, Y. Liu, Z. Liu, L. Zhou, L. Tang, Heterogeneous parallel computing accelerated iterative subpixel digital image correlation, Science China Technological Sciences, 61 (2018) 74-85.

[6] J. Yang, J. Huang, Z. Jiang, S. Dong, L. Tang, Y. Liu, Z. Liu, L. Zhou, SIFT-aided path-independent digital image correlation accelerated by parallel computing, Optics and Lasers in Engineering, 127 (2020) 105964.

[7] J. Yang, J. Huang, Z. Jiang, S. Dong, L. Tang, Y. Liu, Z. Liu, L. Zhou, 3D SIFT aided path independent digital volume correlation and its GPU acceleration, Optics and Lasers in Engineering, 136 (2021) 106323.
