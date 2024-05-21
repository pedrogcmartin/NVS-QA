# NVS Methods Information

From several NVS methods that have been proposed in the past, a subset was selected according to the synthesis performance, training and synthesis speed, and suitability to the considered scene classes, nameley: DVGO, Instant-NGP, Mip-NeRF 360, Nerfacto, NeRF++, Plenoxels, and TensoRF [1,2,3,4,5,6,7].

| NVS Method                                                           | Description |
|:--------------------------------------------------------------------:|:------------|
| [DVGO]](https://sunset1995.github.io/dvgo/)                          | Text        |
| [Instant-NGP](https://nvlabs.github.io/instant-ngp/)                 | Text        |
| [Mip-NeRF 360](https://jonbarron.info/mipnerf360/)                   | Text        |
| [NeRF++](https://github.com/Kai-46/nerfplusplus)                     | Text        |
| [Nerfacto](https://docs.nerf.studio/nerfology/methods/nerfacto.html) | Text        |
| [TensoRF](https://apchenstu.github.io/TensoRF/)                      | Text        |

The table above presents a summarized description of each selected NeRF method. The scene classes to which they were applied are described bellow. 

The NVS methods selected for the 360º real scenes were:
+ DVGO [1]
+ Mip-NeRF 360 [3]
+ Nerfacto [4]
+ NeRF++ [5] 

The NVS methods selected for the 360º synthetic scenes were:
+ DVGO [1]
+ Instant-NGP [2]
+ Plenoxels [6]
+ TensoRF [7]

The NVS methods selected for the FF real scenes were:
+ DVGO [1]
+ Mip-NeRF 360 [3]
+ Nerfacto [4]
+ NeRF++ [5] 

The NVS methods selected for the FF synthetic scenes were:
+ DVGO [1]
+ Instant-NGP [2]
+ Mip-NeRF 360 [3]
+ Nerfacto [4]
+ NeRF++ [5] 
+ TensoRF [7]

Scene classes for which the resulting view synthesis quality was far below acceptable, were excluded from the study; this was the case for Instant-NGP, Plenoxels, and TensoRF with real scenes. Plenoxels was only applied to 360º synthetic due to its design and performance similarities with the DVGO method. Moreover, it is worthy to note that NeRF++, Mip-NeRF 360, and Nerfacto were specifically designed for unbounded scenes; the first two (NeRF++ and Mip-NeRF 360) for 360º unbounded scenes. The remaining methods (Instant-NGP, DVGO, Plenoxels, and TensoRF) were not targeted to a specific scene class, but are more suitable for the synthetic scenes synthesis; furthermore, due to the use of 3D voxel grids in these methods, the training/synthesis times are significantly reduced compared to NeRF++ and Mip-NeRF 360.

# References

[1] C. Sun, M. Sun, and H.-T. Chen, “Direct Voxel Grid Optimization: Super-Fast Convergence for Radiance Fields Reconstruction,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2022, pp. 5459–5469.

[2] T. Müller, A. Evans, C. Schied, and A. Keller, “Instant neural graphics primitives with a multiresolution hash encoding,” in ACM Trans. Graph., vol. 41, no. 4, p. 102:1-102:15, Jul. 2022, doi: 10.1145/3528223.3530127.

[3] J. T. Barron, B. Mildenhall, D. Verbin, P. P. Srinivasan, and P. Hedman, “Mip-NeRF 360: Unbounded Anti-Aliased Neural Radiance Fields,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2022, pp. 5470–5479.

[4] M. Tancik et al., “Nerfstudio: A Modular Framework for Neural Radiance Field Development.” arXiv, Feb. 08, 2023. doi: 10.48550/arXiv.2302.04264.

[5] K. Zhang, G. Riegler, N. Snavely, and V. Koltun, “NeRF++: Analyzing and Improving Neural Radiance Fields.” arXiv, Oct. 21, 2020. doi: 10.48550/arXiv.2010.07492.

[6] S. Fridovich-Keil, A. Yu, M. Tancik, Q. Chen, B. Recht, and A. Kanazawa, “Plenoxels: Radiance Fields Without Neural Networks,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2022, pp. 5501–5510.

[7] A. Chen, Z. Xu, A. Geiger, J. Yu, and H. Su, “TensoRF: Tensorial Radiance Fields,” in Computer Vision – ECCV 2022, S. Avidan, G. Brostow, M. Cissé, G. M. Farinella, and T. Hassner, Eds., in Lecture Notes in Computer Science. Cham: Springer Nature Switzerland, 2022, pp. 333–350. doi: 10.1007/978-3-031-19824-3_20.