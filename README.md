### This Python script is designed to automatically generate MPR images in JPEG format from contrast-enhanced CT DICOM data.
<img width="612" alt="MPR" src="https://github.com/user-attachments/assets/ba3ec47d-0038-4474-8f51-0324b80f2f87" />

Using the `pydicom` module in Python, this script aggregates the data into a 3D array in Numpy format. The information from this 3D array is then output as JPEG images using `matplotlib`. The number of images that can be generated corresponds to the number of original DICOM slices in the axial direction, 512 images in the coronal direction, and 512 images in the sagittal direction.

**Required Python Modules**  

The following Python modules are required, so please make sure to install them in advance.  
`pydicom` `numpy` `matplotlib` `sys` `glob` `pathlib`

**Method**
1. Assign the path of the first file in the DICOM data to `path_ct`. Specify the directory to save the generated MPR images in `storage_path`.
2. Run cells 1 to 3 and take note of the information obtained along the way.
3. Run the fourth cell and adjust the values of `k` and `l` using the sliders to obtain the desired image.　

<img width="612" alt="Window setting" src="https://github.com/user-attachments/assets/a2628b4f-7504-46dc-a07b-5d3b437ae7fc" />

4. Take the values of `k` and `l` obtained from the fourth cell and substitute them into the fifth cell as `Vmin = l - k` and `Vmax = l + k`.　(In this demonstration, `k` was set to 320 and `l` to 1080, resulting in `Vmin` being 760 and `Vmax` being 1400.)  
When you run the cell, new folders named `A`, `C`, and `S` will be created in the specified folder, and the generated JPEG files will be saved inside them.


