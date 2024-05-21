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

For more information about:

+ [Selected Visual Scenes](https://github.com/pedrogcmartin/NVS-QA-Database/blob/main/docs/scenes.md)
+ [Selected NVS Methods](https://github.com/pedrogcmartin/NVS-QA-Database/blob/main/docs/methods.md)
+ [Selected Quality Metrics](https://github.com/pedrogcmartin/NVS-QA-Database/blob/main/docs/metrics.md)

# Citation

(**Alterar**) P. Martin, A. Rodrigues, J. Ascenso and M. P. Queluz, "NeRF-QA: Neural Radiance Fields Quality Assessment Database," 2023 15th International Conference on Quality of Multimedia Experience (QoMEX), Ghent, Belgium, 2023, pp. 107-110, doi: 10.1109/QoMEX58391.2023.10178625.