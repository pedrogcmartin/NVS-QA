# Visual Scenes Information

The real scenes selected from the *Front-Facing* dataset were:
+ *Antique* (351 training images with 960x540 pixels each)
+ *Flowers* (377 training images with 960x540 pixels each)
+ *Playground2* (291 training images with 960x540 pixels each)
+ *Statue* (228 training images with 960x540 pixels each)

The synthetics scenes selected from *Front-Facing* dataset were:
+ *Classroom* (300 training images with 960x540 pixels each)
+ *Mugs* (300 training images with 960x540 pixels each)
+ *Office* (300 training images with 960x540 pixels each)
+ *Tea* (300 training images with 960x540 pixels each)

The selected videos from *Tanks and Temples* dataset were:
+ *M60* (277 training images with 1077×546 pixels each)
+ *Playground* (275 training images with 1008×548 pixels each)
+ *Train* (258 training images with 982×546 pixels each)
+ *Truck* (226 training images with 980×546 pixels each)

The scenes selected from *Realistic Synthetic 360º* dataset were:
+ *Drums* (100 training images with 800×800 pixels each)
+ *Ficus* (100 training images with 800×800 pixels each)
+ *Lego* (100 training images with 800×800 pixels each)
+ *Ship* (100 training images with 800×800 pixels each) 

For the subjective test purpose, the spatial resolutions of the real and FF scenes were uniformized with a cropping to 928×522 pixels.

The selected 360º datasets (namely: [Tanks and Temples](https://www.tanksandtemples.org) and [Realistic Synthetic 360](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1)) have already been used in published works, enabling the validation of the herein generated synthesized videos, by comparison of the obtained objective quality metrics values (using PSNR, SSIM, and LPIPS) with the values reported on those works. Lastly, the 360º synthetic scenes were also synthesized for the case where a subsampling with a factor of 2 was applied to the training set, seeking synthesized video qualities covering the lowest qualities range.