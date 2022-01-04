# FDD_PP
## Frequency Domain Decomposition (FDD), including Peak Picking (PP) technique.
The FDD is a popular method used in structural health monitoring. It is a modal analysis technique which generates a system realization using the frequency response given output measurements.

## Content
Given a set of accelerograms of time series data, the FDD method used in these scripts involves first estimating the power spectral density (PSD) matrices, and then perform their singular value decomposition (SVD). After this, the eigenfrequencies can be determined, either manually or automatically.<br>
<br>
This script computes the SVD from the cross PSD, obtained from the raw time series data. Then, a PP algorithm is used to automatically pick the modal eigenfrequencies peaks from the first singular vector, provided they are not too close to each other. Peaks are selected according to their magnitude, in descending steps. <br>
<br>
The FDD make use of the python pandas, numpy and scipy libraries.<br>
<br>
The input data file consists of a csv file. Each column corresponds to an accelerogram. The first rows might correspond to a header, which can be ignored. <br>
The input parameters are contained in the inputs_fdd.py, as follows: <br>
- folder_inp: input folder name <br>
- file_inp: data input file name <br>
- folder_out: output folder name <br>
- h_cor: Do not consider first h_cor rows (Header) <br>
- Freq: Sample Frequency [Hz] <br>
- npers: Length of each segment <br>
- freq_r_L: Frequency range Low value [Hz] <br>
- freq_r_H: Frequency range High value [Hz] <br>
- dist: Min distance between peaks - samples between neighbouring peaks <br>
- limit_frq: Maximum amount of frequencies to present <br>

## References
[1] Brincker, R., Zhang, L., & Andersen, P. (2001). Modal identification of output-only systems using frequency domain decomposition. Smart materials and structures, 10(3), 441. doi:10.1088/0964-1726/10/3/303.<br>
[2] https://www.mathworks.com/matlabcentral/fileexchange/50988-frequency-domain-decomposition-fdd <br>
[3] https://github.com/AACsempre/FDD
