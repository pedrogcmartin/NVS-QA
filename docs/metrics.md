# Objective Quality Metrics Information


From several NVS methods that have been proposed in the past, a subset was selected according to the synthesis performance, training and synthesis speed, and suitability to the considered scene classes, nameley: DVGO, Instant-NGP, Mip-NeRF 360, Nerfacto, NeRF++, Plenoxels, and TensoRF [1,2,3,4,5,6,7].


| Metric        | Color Space | Description                                                                                                   |
|:-------------:|:-----------:|:--------------------------------------------------------------------------------------------------------------|
| MSE           | RGB         | Average squared difference between corresponding pixels of the two images                                      |
| PSNR-Y        | Y           | Ratio between the maximum power of the image luminance component, and the power of its distortion, measured by the MSE |
| PSNR-YUV      | YUV         | PSNR applied on the YUV color space                                                                            |
| PSNR-HVS [40] | Y           | PSNR with the MSE computed in the DCT domain, using frequency dependent weights                                |
| SSIM [5]      | Y           | Quantifies the similarity between the two images in terms of luminance, contrast, and structure                |
| MS-SSIM [6]   | Y           | Multi-scale variation of SSIM                                                                                  |
| IW-SSIM [41]  | Y           | A variation of SSIM using information content weighted pooling                                                 |
| VIF [42]      | Y           | Considers natural scene statistics in the wavelet domain for content fidelity comparison between the two images |
| VIFp [42]     | Y           | Pixel domain version of VIF                                                                                    |
| FSIM [43]     | LAB         | Normalized average value of features similarity between the two images                                         |
| VSI [44]      | RGB         | Uses visual saliency information both as a quality feature and as a weighting function at the pooling stage     |
| MAD [45]      | Y           | Models adaptive strategies of the human visual system, combining a distortion detection strategy and an appearance-based strategy |
| LPIPS [7]     | RGB         | Measures the perceptual similarity between the two images, based on neural network learned features             |
| ST-LPIPS [48] | RGB         | A variation of LPIPS tolerant to small pixel disparities among between the two images                          |
| DISTS [49]    | RGB         | Structure and texture similarity measurements (SSIM-like) between corresponding feature maps of the two images  |
| GMSD [46]     | Y           | Computes the pixel-wise gradient magnitude similarity (GMS) between two images, followed by pooling based on the standard deviation of the GMS map |
| NLPD [47]     | Y           | Mimics the nonlinear transformations of the early visual system, as local luminance subtraction and local gain control, and combines these values using weighted lp-norms |
| VMAF [50]     | YUV         | Merges existing metrics and image feature components using a support vector machine                             |
| FovVideoVDP [8] | RGB       | Considers spatial, temporal, and peripherical aspects related with the foveate vision effect                    |


The table above presents a summarized description of each selected NeRF method. The scene classes to which they were applied are described bellow.

# References

[1] C. Sun, M. Sun, and H.-T. Chen, “Direct Voxel Grid Optimization: Super-Fast Convergence for Radiance Fields Reconstruction,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2022, pp. 5459–5469.

[2] T. Müller, A. Evans, C. Schied, and A. Keller, “Instant neural graphics primitives with a multiresolution hash encoding,” in ACM Trans. Graph., vol. 41, no. 4, p. 102:1-102:15, Jul. 2022, doi: 10.1145/3528223.3530127.

[3] J. T. Barron, B. Mildenhall, D. Verbin, P. P. Srinivasan, and P. Hedman, “Mip-NeRF 360: Unbounded Anti-Aliased Neural Radiance Fields,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2022, pp. 5470–5479.

[4] M. Tancik et al., “Nerfstudio: A Modular Framework for Neural Radiance Field Development.” arXiv, Feb. 08, 2023. doi: 10.48550/arXiv.2302.04264.

[5] K. Zhang, G. Riegler, N. Snavely, and V. Koltun, “NeRF++: Analyzing and Improving Neural Radiance Fields.” arXiv, Oct. 21, 2020. doi: 10.48550/arXiv.2010.07492.

[6] S. Fridovich-Keil, A. Yu, M. Tancik, Q. Chen, B. Recht, and A. Kanazawa, “Plenoxels: Radiance Fields Without Neural Networks,” in Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, 2022, pp. 5501–5510.

[7] A. Chen, Z. Xu, A. Geiger, J. Yu, and H. Su, “TensoRF: Tensorial Radiance Fields,” in Computer Vision – ECCV 2022, S. Avidan, G. Brostow, M. Cissé, G. M. Farinella, and T. Hassner, Eds., in Lecture Notes in Computer Science. Cham: Springer Nature Switzerland, 2022, pp. 333–350. doi: 10.1007/978-3-031-19824-3_20.

[8] A. Knapitsch, J. Park, Q.-Y. Zhou, and V. Koltun, “Tanks and temples: benchmarking large-scale scene reconstruction,” in ACM Trans. Graph., vol. 36, no. 4, p. 78:1-78:13, Jul. 2017, doi: 10.1145/3072959.3073599.

[9] B. Mildenhall, P. P. Srinivasan, M. Tancik, J. T. Barron, R. Ramamoorthi, and R. Ng, “NeRF: representing scenes as neural radiance fields for view synthesis,” in Commun. ACM, vol. 65, no. 1, pp. 99–106, Dec. 2021, doi: 10.1145/3503250.

[10] B. Foundation, “Blender - a 3D modelling and rendering package.” Stichting Blender Foundation, Amsterdam, 2018.

[11] ITU-R, “BT.500-14: Methodologies for the subjective assessment of the quality of television images,” 2019.
