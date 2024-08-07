# Passive_CardioVascular_Model_CPR
Simscape model of cardiovascular system under cardiac arrest to find better CPR technique

This is an improved version of our earlier passive cardiovascular model to test different CPR techniques. To run our model, you have to build custom library in your own system in the Simscape® environment. The method to build that custom block is as follow:

Instructions to build the library: 

A – Replace Branch.ssc file from the Hydraulic library
copy the branch.ssc file
Replace the branch.ssc file located in: MATLAB_R2020a/toolbox/physmod/simscape/library/m/+foundation/+hydraulic

B – Download and build the Cardiovascular library
Take the +Cardiovascular folder and add it to the following path: MATLAB_R2020a/toolbox/physmod/simscape/library/m.
Open any of the .ssc files on MATLAB and change the current folder to: MATLAB_R2020a/toolbox/physmod/simscape/library/m/+Cardiovascular
Build the library by executing the “ssc_build” command in the Command window or follow the instructions on the relative documentation: https://www.mathworks.com/help/physmod/simscape/ref/ssc_build.html
The Cardiovascular_lib.slx file should become visible in the /m directory and ready to use. NOTE: use Matlab_R20020a for these files to run properly because I generate these libraraies at R20020a version

Notes: a) Windows users may need to have full writing permissions of the MATLAB_R2020a/toolbox/physmod/simscape/library directory. b) If the following error occurs: Failed to generate ‘Cardiovascular_lib’, caused by: error using feval, unrecognized function of variable “Cardiovascular.variable_c_chamber” change the name of the file giving the error (both .ssc and .svg) as well as that in the block definition (line #1 of code), and ensure that they are given exactly the same name. Run again the ssc_build command to build the library.

See documentation on Hydraulic library elements on: https://www.mathworks.com/help/physmod/hydro/hydraulics- modeling.html?s_tid=CRUX_lftnav
