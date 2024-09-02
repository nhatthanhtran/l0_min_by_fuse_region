# Python wrapper for Fast l0 minimization by fusion region

This is a python wrapper for the paper [Fast and Effective L0 Gradient Minimization by Region Fusion](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Nguyen_Fast_and_Effective_ICCV_2015_paper.pdf) by Rang Nguyen, and Michael Brown.

### Citation
If you find this wrapper useful for your research please cite the paper.
```
@inproceedings{nguyen2015fast,
  title={Fast and effective L0 gradient minimization by region fusion},
  author={Nguyen, Rang MH and Brown, Michael S},
  booktitle={Proceedings of the IEEE international conference on computer vision},
  pages={208--216},
  year={2015}
}
```

### File structure
This folder contain:
- Example Image: country_house.jpg
- Example Python code: python_l0.py
- L0 module wrapper: l0_module.cpython-39-x86_64-linux-gnu.so

### How to use
Copy the L0 module wrapper into your python directory. In your python code, import the module
by import l0_module. If you save the L0 module in 
another directory then point your import to the 
correct folder. 

After import the module, you can use it directly as:

l0_module.main_l0(image_file_in, lambda, image_file_out)

where 
image_file_in: (string) the location where the image you want to process

lambda: (float) the hyper-parameter to process the image

image_file_out: (string) the location where the 
outoput image will be saved

For example:
import l0_module

l0_module.main_l0(i"country_house.jpg",0.2,"country_house_example.png")
