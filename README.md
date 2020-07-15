# Ring Oscillator Measurements Spartan 3E

We have collected on-chip variability data of nearly 200 Spartan 3E FPGAs (90nm), designed functional prototypes of PUFs,
analyzed aging effects, and created improved entropy extraction methods. This repository provides access to our measurement data.

The analysis of the dataset is described in the following [publication](https://schaumont.dyn.wpi.edu/schaum//pdf/papers/2010hostm.pdf).

~~~
A. Maiti, J. Casarona, L. McHale, P. Schaumont, "A Large Scale Characterization of RO-PUF," 
IEEE International Symposium on Hardware-Oriented Security and Trust (HOST 2010), Anaheim, June 2010.
~~~

## Data Format

In each file, there are 512 lines for 512 ROs. Each of the line contains 100 RO frequencies separated by comma. These are 100 samples of the corresponding RO. The frequency values are expressed in Hz.

It is important to describe the spatial location of the ROs. The 2-D RO array has 32 rows and 16 columns. The first RO (first line in the csv file) is located at the CLB location X10Y8 (SLICE_X18Y14:SLICE_X19Y15), and the 16th RO (16th line in the csv file) is located at CLB X25Y8 (SLICE_X48Y14:SLICE_X49Y15). The intermediate 14 ROs are located across CLB location X11Y8 to CLB location X24Y8.

Similarly, the second row starts with the 17th RO (17th line in the csv file) at CLB location X10Y9 and ends with the 32nd RO (32nd line in the csv file) at the CLB location X25Y9. Likewise, the 512th RO (the last line in the csv file) is located at the CLB location X25Y39.

