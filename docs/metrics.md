# Objective Quality Metrics Information

The objective quality metrics selection was based on several criteria, notably: i) metrics that are typically applied in the NVS literature, namely PSNR-Y, PSNR-YUV, SSIM [1], MS-SSIM [2], LPIPS [3], and FovVideoVDP [4], since it is important to know whether they are in fact suitable for assessing the quality of NVS content; ii) metrics that have shown good performance in several image and video applications, such as PSNR-HVS [5], IW-SSIM [6], VIF and VIFp [7], FSIM [8], VSI [9], MAD [10], GMSD [11], and NLPD [12]; iii) learning-based metrics (besides LPIPS), namely ST-LPIPS [13], DISTS [14], and VMAF [15]; iv) MSE, since every selected NVS method includes it in the loss function. All metrics are full-reference.

Certainly! Here is the table with the references corrected according to the new bibliography order:

| Metric        | Color Space | Description                                                                                                   |
|:-------------:|:-----------:|:--------------------------------------------------------------------------------------------------------------|
| [MSE](https://scikit-image.org/docs/stable/api/skimage.metrics)           | RGB         | Average squared difference between corresponding pixels of the two images                                      |
| [PSNR-Y](https://scikit-image.org/docs/stable/api/skimage.metrics)        | Y           | Ratio between the maximum power of the image luminance component, and the power of its distortion, measured by the MSE |
| [PSNR-YUV](https://scikit-image.org/docs/stable/api/skimage.metrics)      | YUV         | PSNR applied on the YUV color space                                                                            |
| [PSNR-HVS](https://pypi.org/project/psnr-hvsm) [5] | Y           | PSNR with the MSE computed in the DCT domain, using frequency dependent weights                                |
| [SSIM](https://pypi.org/project/sewar) [1]      | Y           | Quantifies the similarity between the two images in terms of luminance, contrast, and structure                |
| [MS-SSIM](https://pypi.org/project/sewar) [2]   | Y           | Multi-scale variation of SSIM                                                                                  |
| [IW-SSIM](https://github.com/Jack-guo-xy/Python-IW-SSIM) [6]  | Y           | A variation of SSIM using information content weighted pooling                                                 |
| [VIF](https://pypi.org/project/sewar) [7]      | Y           | Considers natural scene statistics in the wavelet domain for content fidelity comparison between the two images |
| [VIFp](https://pypi.org/project/sewar) [7]     | Y           | Pixel domain version of VIF                                                                                    |
| [FSIM](https://pypi.org/project/IQA-pytorch) [8]     | LAB         | Normalized average value of features similarity between the two images                                         |
| [VSI](https://pypi.org/project/IQA-pytorch) [9]      | RGB         | Uses visual saliency information both as a quality feature and as a weighting function at the pooling stage     |
| [MAD](https://pypi.org/project/IQA-pytorch) [10]      | Y           | Models adaptive strategies of the human visual system, combining a distortion detection strategy and an appearance-based strategy |
| [LPIPS](https://github.com/richzhang/PerceptualSimilarity) [3]     | RGB         | Measures the perceptual similarity between the two images, based on neural network learned features             |
| [ST-LPIPS](https://pypi.org/project/IQA-pytorch) [13] | RGB         | A variation of LPIPS tolerant to small pixel disparities among between the two images                          |
| [DISTS](https://github.com/dingkeyan93/DISTS) [14]    | RGB         | Structure and texture similarity measurements (SSIM-like) between corresponding feature maps of the two images  |
| [GMSD](https://pypi.org/project/IQA-pytorch) [11]     | Y           | Computes the pixel-wise gradient magnitude similarity (GMS) between two images, followed by pooling based on the standard deviation of the GMS map |
| [NLPD](https://pypi.org/project/IQA-pytorch) [12]     | Y           | Mimics the nonlinear transformations of the early visual system, as local luminance subtraction and local gain control, and combines these values using weighted lp-norms |
| [VMAF](https://github.com/Netflix/vmaf) [15]     | YUV         | Merges existing metrics and image feature components using a support vector machine                             |
| [FovVideoVDP](https://github.com/gfxdisp/FovVideoVDP) [4] | RGB       | Considers spatial, temporal, and peripherical aspects related with the foveate vision effect                    |

**Note:** Each metric's name has an hyperlink for the corresponding implementation used in this study.

Most of the selected metrics were designed for the quality assessment of still images (IQA metrics), with FovVideoVDP and VMAF being the exceptions as they were specifically tailored for video (VQA metrics). In this paper, the latter were directly applied to the reference and synthesized videos, whereas the former were applied to individual frames of both videos, followed by the averaging of the frame-based quality scores to obtain a global video score. In terms of the metrics implementation, while for DISTS, FovVideoVDP, IW-SSIM, LPIPS, PSNR-HVS, and VMAF the code was provided by the authors in their respective publications were used for the remaining metrics. The table above presents a comprehensive overview of the selected metrics, including their succinct descriptions, reference to the source code, and the used color space. As suggested in [16], [17], a disparity compensation should be performed between synthesized and reference images before applying conventional quality metrics (such as SSIM). In fact, even though the MRE is around 0.86 and 1.04 pixels for 360º real and FF real scenes, respectively, the NeRF pipeline may lead to an amplification effect of the pose errors negative impact on the synthesized view. Thus, the object shifts from the ground-truth to the synthesized image can be significantly higher than the corresponding MRE. Disparity compensation is performed with block-matching algorithm with a macroblock size of 32×32 pixels and search parameter of 12 pixels (except for the NeRF++ synthesized sequences of the antique and flowers scenes, where a value of 50 pixels was selected as disparities of more than 12 pixels were present).

# References

[1] Z. Wang, A. C. Bovik, H. R. Sheikh, and E. P. Simoncelli, “Image quality assessment: from error visibility to structural similarity,” IEEE Trans. Image Process., vol. 13, no. 4, pp. 600–612, Apr. 2004.

[2] Z. Wang, E. Simoncelli, and A. Bovik, “Multiscale structural similarity for image quality assessment,” in Asilomar Conference on Signals, Systems and Computers (ACSSC), Pacific Grove, CA, USA, Dec. 2003, pp. 1398-1402 Vol.2.

[3] R. Zhang, P. Isola, A. A. Efros, E. Shechtman, and O. Wang, “The Unreasonable Effectiveness of Deep Features as a Perceptual Metric,” in Proc. IEEE/CVF Conf. Comput. Vis. Pattern Recognit. (CVPR), Salt Lake City, UT, USA, Jun. 2018, pp. 586–595.

[4] R. K. Mantiuk et al., “FovVideoVDP: a visible difference predictor for wide field-of-view video,” ACM Trans. Graph., vol. 40, no. 4, p. 49:1-49:19, Jul. 2021.

[5] P. Gupta, P. Srivastava, S. Bhardwaj, and V. Bhateja, “A modified PSNR metric based on HVS for quality assessment of color images,” in IEEE Int. Conf. Communication and Industrial Application (ICCIA), Kolkata, India, Dec. 2011, pp. 1–4.

[6] Z. Wang and Q. Li, “Information Content Weighting for Perceptual Image Quality Assessment,” IEEE Trans. Image Process., vol. 20, no. 5, pp. 1185–1198, May 2011.

[7] H. R. Sheikh and A. C. Bovik, “Image information and visual quality,” IEEE Trans. Image Process., vol. 15, no. 2, pp. 430–444, Feb. 2006.

[8] L. Zhang, L. Zhang, X. Mou, and D. Zhang, “FSIM: A Feature Similarity Index for Image Quality Assessment,” IEEE Trans. Image Process., vol. 20, no. 8, pp. 2378–2386, Aug. 2011.

[9] L. Zhang, Y. Shen, and H. Li, “VSI: A Visual Saliency-Induced Index for Perceptual Image Quality Assessment,” IEEE Trans. Image Process., vol. 23, no. 10, pp. 4270–4281, Oct. 2014.

[10] E. Larson and D. Chandler, “Most apparent distortion: Full-reference image quality assessment and the role of strategy,” J. Electron. Imaging, vol. 19, p. 011006, Jan. 2010.

[11] B. Zhang, P. V. Sander, and A. Bermak, “Gradient magnitude similarity deviation on multiple scales for color image quality assessment,” in Proc. IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP), New Orleans, LA, USA, Mar. 2017, pp. 1253–1257.

[12] V. Laparra, A. Berardino, J. Ballé, and E. P. Simoncelli, “Perceptually optimized image rendering,” J. Opt. Soc. Am. A, vol. 34, no. 9, pp. 1511–1525, Sep. 2017.

[13] A. Ghildyal and F. Liu, “Shift-Tolerant Perceptual Similarity Metric,” in European Conference on Computer Vision (ECCV), Berlin, Heidelberg: Springer-Verlag, Oct. 2022, pp. 91–107.

[14] K. Ding, K. Ma, S. Wang, and E. P. Simoncelli, “Image Quality Assessment: Unifying Structure and Texture Similarity,” IEEE Trans. Pattern Anal. Mach. Intell., vol. 44, no. 5, pp. 2567–2581, May 2022.

[15] Z. Li, A. Aaron, I. Katsavounidis, A. Moorthy, and M. Manohara, “Toward A Practical Perceptual Video Quality Metric,” Medium, Apr. 2017.

[16] E. Bosc et al., “Towards a New Quality Metric for 3-D Synthesized View Assessment,” IEEE J. Sel. Top. Signal Process., vol. 5, no. 7, pp. 1332–1343, Nov. 2011.

[17] C.-T. Tsai and H.-M. Hang, “Quality assessment of 3D synthesized views with depth map distortion,” in 2013 Visual Communications and Image Processing (VCIP), Nov. 2013, pp. 1–6.
