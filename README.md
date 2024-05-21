# NVS-QA Database

NeRF View Synthesis: Subjective Quality Assessment and Objective Metrics Evaluation

Pedro Martin, António Rodrigues, João Ascenso, Maria Paula Queluz  
Instituto de Telecomunicações, Instituto Superior Técnico, University of Lisbon

The NVS-QA database contains: 

+ Synthesized videos of the same test time interval of the reference videos due to the camera paths available information (in the "Synthesized Videos" folder);
+ Reference videos of the visual scenes (in the "Reference Videos" folder), with durations of 10s (and of 8s for 360º synthetics scenes);
+ Results of a subjective study comparing the qualities of the reference and synthesized videos by a group of 22 participants (in the "DMOS.xlsx" file);
+ Quality prediction results of a selection of 19 objective quality metrics on the reference and synthesized material (in the "metrics.xlsx" file);
+ Training dataset used for the NVS methods training (in the "Front-facing Dataset" folder) with eight, real and synthetic, front-facing (FF) camera acquisition visual scenes;
+ Camera paths with the pose estimation of the reference videos enabling the creation of synthesized videos with the same camera path (in the "Camera Paths" folder).

![DSCQS](https://github.com/pedrogcmartin/NeRF-QA-Database/blob/main/github%20images/DSCQS.jpg)

+ Selected Visual Scenes ([Scenes](https://github.com/pedrogcmartin/NVS-QA-Database/blob/main/docs/scenes.md))
+ Selected NVS Methods ([Methods](https://github.com/pedrogcmartin/NVS-QA-Database/blob/main/docs/methods.md))


The Double Stimulus Continous Quality Scale (DSCQS) was selected as an evaluation method. A total of 88 pairs of stimulus (56 synthesized synthetic videos + 32 synthesized real videos, together with the respective original videos) were assessed. After the test, the resulting scores were processed according to [11] to obtain Differential Mean Opinion Score (DMOS) values for each synthesized video. More details about the subjective assessment procedure can be found in [11].


Cortes:

 that are used to train seven NeRF based methods (nameley: DVGO, Instant-NGP, Mip-NeRF 360, Nerfacto, NeRF++, Plenoxels, and TensoRF [1,2,3,4,5,6,7])

# Citation

(ArXiv reference and link)

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
