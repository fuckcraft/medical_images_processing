# Medical images processing
----

## Medical file format to avi

### 1.DICOM to AVI

dicom2avi function (which is a matlab program) converts dicom file to avi. It needs third party function -natsortfiles function (see http://cn.mathworks.com/matlabcentral/fileexchange/34464-customizable-natural-order-sort ) ,and this function is compiled by matlab 2016a.

### 2.NIFTI to AVI

NIfTI2avi.m function convert nii format file to avi or mp4 format. It needs third party function: load_nii.m, reslice_nii.m and view_nii.m (see http://cn.mathworks.com/matlabcentral/fileexchange/8797-tools-for-nifti-and-analyze-image ) ,and this function is compiled by matlab 2016a.

----
## MGZ Processing

This folder contains several functions and files. <br>
The source code downloaded from [Xiangrui Li's program](https://cn.mathworks.com/matlabcentral/fileexchange/42997-dicom-to-nifti-converter--nifti-tool-and-viewer "Click to show source code"). And I modify his code to my program, including nii_tool.m (where I delete save nii function, and add nii parameter to return.) and dicm2nii.m (where I rename it to mgz_processing.m, and change many functions ). Also,  due to functional unit reduction (only aim to extract mgz data.), I delete many functions and files from source code. <br>
I `did not` optimize these functions yet, but more changes will be taken in the future. <br>

The 002_S_0729 folder contains a original datum (brainmask.mgz) which downloaded from [ADNI database](http://adni.loni.usc.edu/ "Click to skip"), and some results, such as brainmask.nii, sample.mat and sample.bmp.
You can use mgz_example.m to know the basic usage of this program. <br>

The image above is a frame of mgz data.
![Frame Sample](https://github.com/fuckcraft/medical_images_processing/raw/master/mgz_processing/002_S_0729/sample.bmp "Extract from original_data")

### Note:
I change mgz_processing.m function a lot. Its input parameter can only use mgz format, and output parameter can only use nii format. <br>
The returned parameters: name (cell); file_details (structure); nii_data (structure); original_data (matrix) . <br>
For the details, please see function and mgz_example.m.
