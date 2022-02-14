# CAG-D-21-00842
<b>Elliptic Gabriel Smoothing of Point Clouds</b> accompanying software<br />
<br />
A CMAKE and a Microsoft VS2019 solution is given.<br />
Please note that the VS solution uses the CUDA 11.6 target. If your CUDA version is different<br />
you need with a text editor edit the file EGTSmoothingVS2019.vcxproj<br />
and replace in the two lines:<br />
<i>Import Project="$(VCTargetsPath)\BuildCustomizations\CUDA 11.6.props"</i><br />
<i>Import Project="$(VCTargetsPath)\BuildCustomizations\CUDA 11.6.targets"</i><br />
The cuda version you have.<br />
Also please set appropriately the environmental variables $(BOOST_DIR), $(CGAL_INCLUDE).<br />
<br />
If a binary executable is successfully acquired, for example EGTSmoothingVS2019.exe, the program is run as:<br />
<br />
EGTSmoothingVS2019.exe cad_complex_noise.xyz 75 0.63 -0.64 0.75 0 cad_complex_smoothed_egt.xyz<br />
<br/>
The first argument is the point cloud to be smoothed which is a text file of points of the form "x y z nx ny nz" for each line (x, y, z the point coordinates, nx, ny, nz the normal coordinates).<br />
The second argument is the number of iterations EGT will be performed.<br />
The third argument is the lambda parameter.<br />
The fourth argument is the mu parameter.<br />
The fifth parameter is the alpha parameter.<br />
The sixth parameter (set to zero in our paper), 0 for use of the Gaussian weights of the paper.<br />
The seventh parameter is the target smoothed point cloud as a text file of the form "x y z" for each line.
