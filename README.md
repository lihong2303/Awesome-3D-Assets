<h1 align="center">
🔥Awesome-3D-Assets
</h1>

A repository for recent 3D Assets.

🫨 Working hard on collecting ...

A incomplete collection of 3D tasks can be found [here](./assets/3D_tasks.md).

# 3D Datasets

## Contents
- [Real Data](#real-data)
    - [Object](#object)
        - [Hands](#hands)
    - [Scene](#scene)
- [Synthetic](#synthetic)
    - [Object](#object-1)
        - [Manipulation](#manipulation)
    - [Scene](#scene-1)
    - [Object and Scene](#object-and-scene)
- [Real and Synthetic](#real-and-synethetic)
    - [Object](#object-2)
    - [Scene](#scene-2)
- [Scene Datasets](#scene-datasets) 
- [Statistics](#statistics)
- [Generative models or tools](#generative-models-or-tools)
    - [Object](#object-3)
        - [Text-2-3D](#text-2-3d)
        - [Single-view-Image-2-3D](#single-view-2-3d)
        - [Paired-Imgaes-2-3D](#pairedimg-2-3d)
        - [Multi-view 2 3D](#multi-view-2-3d)
    - [Scene](#scene-3)
    - [Image](#image)
        - [RGB-2-Depth](#rgb-2-depth)




## Real Data

### Object

| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| CVPR 2024 | [ULIP-2: Towards Scalable Multimodal Pre-training for 3D Understanding](https://arxiv.org/pdf/2305.08275) | Objaverse, ShapeNet | (800K real-world 3D shape),(52.5K 3D shapes with 55 annotated categories) | 3D point clouds, images, and language | zero-shot 3D classification, standard 3D classification with fine-tuning, and 3D captioning (3D-to- language generation) |
| CVPR 2024 Workshop | [3DCoMPaT Challenge](https://3dcompat-dataset.org/workshop/C3DV24/) | 3DCoMPaT dataset++ |  | 3D objects, 3D renderings |  recognize and ground compositions of materials on parts of 3D objects | 
| CVPR 2024 | [LASO: Language-guided Affordance Segmentation on 3D Object](https://openaccess.thecvf.com/content/CVPR2024/papers/Li_LASO_Language-guided_Affordance_Segmentation_on_3D_Object_CVPR_2024_paper.pdf) | 3D-AffordanceNet | 19,751 point-question pairs, covering 8434 object shapes and 870 expert-crafted questions; | Point Cloud, Text | Language-guided Affordance Segmentation on 3D Object |
| NeurlPS 2023 | [OpenShape: Scaling Up 3D Shape Representation Towards Open-World Understanding](https://arxiv.org/pdf/2305.10764) | ShapeNetCore, 3D-FUTURE,ABO, Objaverse| 876 K | Text-image-3D point cloud | point cloud captioning, point-cloud conditioned image generation |
| NeurlPS 2023 | [Real3D-AD: A Dataset of Point Cloud Anomaly Detection](https://arxiv.org/pdf/2309.13226)| Raw | 1,254 high-resolution 3D items (from forty thousand to millions of points for each item) | Point-cloud | 3D industrial anomaly detection | 
| CVPR2023 | [RealImpact: A Dataset of Impact Sound Fields for Real Objects](https://arxiv.org/pdf/2306.09944) | Raw | 150,000 recordings of impact sounds of 50 everyday objects,5 distinct impact positions | impact locations, microphone locations, contact force profiles, material labels, and RGBD images | listener location classification and visual acoustic matching |
| CVPR 2023 | [OMNI3D: A Large Benchmark and Model for 3D Object Detection in the Wild](https://arxiv.org/pdf/2207.10660) | New annotation (SUN RBG-D, ARKitScenes, Hypersim, Objectron, KITTI and nuScenes) | 234k images annotated with more than 3 million instances and 98 3D boxes categories | single-image, 3D cuboids | 3D object detections |
| CVPR 2023 | [OmniObject3D: Large-Vocabulary 3D Object Dataset for Realistic Perception, Reconstruction and Generation](https://openaccess.thecvf.com/content/CVPR2023/papers/Wu_OmniObject3D_Large-Vocabulary_3D_Object_Dataset_for_Realistic_Perception_Reconstruction_and_CVPR_2023_paper.pdf) | Raw | 6,000 scanned objects (190 daily categories) |  Mesh, Point-cloud, multi-view, videos | 3D perception, novel-view synthesis, neural surface reconstruction, 3D object generation | 
| CVPR 2022 | [Self-supervised Neural Articulated Shape and Appearance Models](https://arxiv.org/pdf/2205.08525) | No dataset contribution | - | image, 3D shape | few-shot reconstruction, the generation of novel articulations, and novel view-synthesis |
| CVPR 2022 | [ABO: Dataset and Benchmarks for Real-World 3D Object Understanding](https://openaccess.thecvf.com/content/CVPR2022/papers/Collins_ABO_Dataset_and_Benchmarks_for_Real-World_3D_Object_Understanding_CVPR_2022_paper.pdf) | Raw | 7, 953 3D Mesh; 8,222  multi-view images) | Mesh, Multi-view; attribute | single-view 3D reconstruction, material estimation, and cross-domain multi-view object retrieval. |
| NeurlPS 2022 Dataset and Benchmark | [MBW: Multi-view Bootstrapping in the Wild](https://arxiv.org/pdf/2210.01721) | Raw Dataset | Multi-view (2~4 cameras) tigers, fish, colobus monkeys, gorillas, chimpanzees, and flamingos from a zoo dataset, each with 2 synchronized videos | Multi-view, 2D landmark of articulated objects | Labeling articulated objects |
| CVPR 2021 | [3D AffordanceNet: A Benchmark for Visual Object Affordance Understanding](https://arxiv.org/abs/2103.16397) | PartNet | 23 K with 18 affordance classes | 3D point cloud with affordance annotations | Affordance Reasoning |
| ICCV 2021 | [Common Objects in 3D: Large-Scale Learning and Evaluation of Real-life 3D Category Reconstruction](https://openaccess.thecvf.com/content/ICCV2021/papers/Reizenstein_Common_Objects_in_3D_Large-Scale_Learning_and_Evaluation_of_Real-Life_ICCV_2021_paper.pdf) | Raw (Annotated on MS-COCO)| 1.5 M multi-view (19K objects) <=>(annotation)cameras and 3D point clouds  | Multi-view; Point-cloud |  new-view-synthesis and category-centric 3D reconstruction |
| ECCV 2020| [ReferIt3D: Neural Listeners for Fine-Grained 3D Object Identification in Real-World Scenes](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123460409.pdf) | ScanNet | two datasets (synthetic dataset of referential utterances (Sr3D) and natural referential utterances (Nr3D)): 5878 (Scene target, distractors) tuples | scene, target objects, relationships between target objects and surrounding object (anchor) | lanuage-assisted 3D point clouds |
| ECCV 2016 | [ObjectNet3D: A Large Scale Database for 3D Object Recognition](https://cvgl.stanford.edu/papers/xiang_eccv16.pdf) | Raw | 100 categories, 90,127 images, 201,888 objects, 44,147 3D shapes | Images, 3D shape (not mesh or pc) | 3D pose / 3D shape recognition |
| CVPR 2015 | [3D ShapeNets: A Deep Representation for Volumetric Shapes](https://arxiv.org/pdf/1406.5670) |Raw (download 3D CAD models (3D Warehouse, Yobi3D)) | 3D CAD, categories | 151,128 3D CAD models <=>  660 unique object categories | object recognition and shape completion |
#### Hands
| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| NeurlPS 2023 | [A Dataset of Relighted 3D Interacting Hands](https://proceedings.neurips.cc/paper_files/paper/2023/file/396beafa6feba781a7114780e6837253-Paper-Datasets_and_Benchmarks.pdf) | Raw | 1.5M Images, 10 subobject | image; MANO & Mask | track two-hand 3D poses |

#### Ego

| time      | paper                                                        | Sources | Data Scale  | Modality              | Task               |
| --------- | ------------------------------------------------------------ | ------- | ----------- | --------------------- | ------------------ |
| WACV 2024 | [IKEA Ego 3D Dataset               Understanding furniture assembly actions from ego-view 3D Point Clouds](https://openaccess.thecvf.com/content/WACV2024/html/Ben-Shabat_IKEA_Ego_3D_Dataset_Understanding_Furniture_Assembly_Actions_From_Ego-View_WACV_2024_paper.html) | Raw     | 493k frames | Point cloud, ego RGBD | action recognition |
| T-Ro 2024 | [Towards robust robot 3d perception in urban environments: The ut campus object dataset](https://arxiv.org/abs/2309.13549) | Raw | 58min (1.3M 3D bounding box); 53 categories | Point-cloud, RGB-D, 9 DoF inertial measurements.  | 3D object detection |

### Scene

| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| CVPR 2024 | [Open3DSG: Open-Vocabulary 3D Scene Graphs from Point Clouds with Queryable Objects and Open-Set Relationships](https://openaccess.thecvf.com/content/CVPR2024/papers/Koch_Open3DSG_Open-Vocabulary_3D_Scene_Graphs_from_Point_Clouds_with_Queryable_CVPR_2024_paper.pdf) | 3DSSG | 1482 scene graphs with 48k object nodes and 544k edges; 93 different attributes on 21k object instances; relationship and affordance w/o exact number | RGB-D | 3D object classification and inter-object relationships prediction|
| CVPR 2024 | [Multi-Attribute Interactions Matter for 3D Visual Grounding](https://openaccess.thecvf.com/content/CVPR2024/papers/Xu_Multi-Attribute_Interactions_Matter_for_3D_Visual_Grounding_CVPR_2024_paper.pdf) | ScanRefer, ReferIt3D(Sr3D/Nr3D) | (51K descriptions; 11K objects; 800 ScanNet scenes),(41K human-annotated descriptions/83K simple machine-generated descriptions; 707 scenes with object mask) | RGB-D, language | 3D visual grounding |
| CVPR 2024 | [LASA: Instance Reconstruction from Real Scans using A Large-scale Aligned Shape Annotation Dataset](https://arxiv.org/pdf/2312.12418) | ArKitScenes | 10,412 CAD aligned with 920 scenes across 17 categories scanned from ArKitScene| Point cloud, Multi-view | indoor instance-level scene reconstruction |
| CVPR 2024 | [DL3DV-10K: A Large-Scale Scene Dataset for Deep Learning-based 3D Vision](https://openaccess.thecvf.com/content/CVPR2024/html/Ling_DL3DV-10K_A_Large-Scale_Scene_Dataset_for_Deep_Learning-based_3D_Vision_CVPR_2024_paper.html) | Raw | 10K videos, 51M frames,  with POI annotation | Multi-view RGB | novel view synthesis |
| ICLR 2023 | [SQA3D: Situated Question Answering in 3D Scenes](https://arxiv.org/pdf/2210.07474) | ScanNet (***New Situation Question Answer***)| 6.8K Situation <=> 20.4K description <=> 33.4K Reasoning Answer| 3D scan, egocentric video, bird-eye view <=> situation <=> question |3D Situation Question Answer|
| ICCV 2023 | [ScanNet++: A High-Fidelity Dataset of 3D Indoor Scenes](https://arxiv.org/abs/2308.11417) | Raw | 460 scenes, 280000 DSLR images, 3.7M iPhone RGBD | Point cloud, Mesh, RGBD | novel view synthesis and 3D semantic scene understanding |
| ICCV 2023 | [Multi3DRefer: Grounding Text Description to Multiple 3D Objects](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhang_Multi3DRefer_Grounding_Text_Description_to_Multiple_3D_Objects_ICCV_2023_paper.pdf) | ScanRefer | 61926 descriptions of 11609 objects | | 3D Visual Grounding |
| CVPR 2022 | [ScanQA: 3D Question Answering for Spatial Scene Understanding](https://openaccess.thecvf.com/content/CVPR2022/papers/Azuma_ScanQA_3D_Question_Answering_for_Spatial_Scene_Understanding_CVPR_2022_paper.pdf) | ScanNet (***New Question-Answer Pairs***) | 41 K question-answer pairs (800 indoors scenes) | RGB-D | 3D Question-Answer (spatial understanding) |
| ECCV 2022 | [Language-Grounded Indoor 3D Semantic Segmentation in the Wild***ScanNet200***](https://arxiv.org/pdf/2204.07761) | ScanNet | 200 categories in ScanNet | - | 3D instance segmentation;  | 
| CVPR 2021 | [***Scan2Cap***: Context-aware Dense Captioning in RGB-D Scans](https://openaccess.thecvf.com/content/CVPR2021/papers/Chen_Scan2Cap_Context-Aware_Dense_Captioning_in_RGB-D_Scans_CVPR_2021_paper.pdf) | ScanRefer ***(New Task)*** | 51,583 descriptions for 11,046 objects in 800 ScanNet scenes | RGB-D <=> bounding box <=> descriptions | dense scan in 3D scenes |
| ECCV 2020 | [ScanRefer: 3D Object Localization in RGB-D Scans using Natural Language](https://arxiv.org/abs/1912.08830) | ScanNet (***New Task***) | 51,583 descriptions <=> 11,046 objects | RGB-D 3D Scens; textual; | Object location with text descriptions |
| ICCV 2019 | [RIO: 3D Object Instance Re-Localization in Changing Indoor Environments](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wald_RIO_3D_Object_Instance_Re-Localization_in_Changing_Indoor_Environments_ICCV_2019_paper.pdf) | Raw Data | 1482 RGB-D Scans of 478 environmental | RGB-D <=> object instance <=> 6 DoF mapping among scenes | 3D object instance re-localization (RIO) |
| ArXiv 2019 | [The ***Replica*** Dataset: A Digital Replica of Indoor Spaces](https://arxiv.org/pdf/1906.05797) | Raw | 18 highly photo-realistic 3D indoor scenes | dense mesh; high-resolution high-dynamic range textures <=> semantic class and instance information <=> planar mirror, glass reflectors| 3D instance segmentation; navigation; question-answering; instruction following |
| CVPR 2017 | [ScanNet: Richly-annotated 3D Reconstructions of Indoor Scenes](https://openaccess.thecvf.com/content_cvpr_2017/papers/Dai_ScanNet_Richly-Annotated_3D_CVPR_2017_paper.pdf) | Raw Data | 2.5M in Multi-views in 1513 scene annotations | RGB-D <=> 3D camera pose <=> surface reconstruction <=> semantic segmentation|  3D object classification, semantic voxel labeling, and CAD model retrieval |


## Synthetic


### Object
| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| CVPR 2024| [Paint-it: Text-to-Texture Synthesis via Deep Convolutional Texture Map Optimization and Physically-Based Rendering](https://arxiv.org/pdf/2312.11360)| 
| CVPR 2023 | [GAPartNet: Cross-Category Domain-Generalizable Object Perception and Manipulation via Generalizable and Actionable Parts](https://arxiv.org/pdf/2211.05272) | Raw: GAPartNet| 8489part instances on 1166 objects  | Point-cloud | part segmentation, part pose estimation, and part-based object manipulation |
| NeurIPS 2023  |[3D-Aware Visual Question Answering about Parts, Poses and Occlusions](https://arxiv.org/pdf/2310.17914)| Super-CLEVR-3D |  5 categories with sub-types and attributes (12; color, material, size). | RGB-D | part questions, 3D pose questions, and occlusion questions |
| ArXiv 2212 | [GeoCode: Interpretable Shape Programs](https://arxiv.org/pdf/2212.11715) | - | train: 9,570 chairs, 9,330 vases, and 6,270 tables; validation and test: 957 chairs, 933 vases, and 627 tables | Mesh, Point-Cloud, sketch | 3D geometry edit |
| NeurlPS 2022 Datasets and Benchmarks | [Breaking Bad: A Dataset for Geometric Fracture and Reassembly](https://breaking-bad-dataset.github.io) | Thingi10K, PartNet | 10,474 shapes, 1,047,400 breakdown patterns | Point cloud | geometry measurements; shape assembly |
| CVPR 2022 | [Fixing Malfunctional Objects With Learned Physical Simulation and Functional Prediction](https://arxiv.org/pdf/2205.02834) | Raw Data: poorly-designed 3D physical objects (point videos of 3D objects) with choices to fix them | 5K | Point cloud | fixing 3D object shapes based on functionality |
| ACCV 2022 | [The Eyecandies Dataset for Unsupervised Multimodal Anomaly Detection and Localization](https://arxiv.org/pdf/2210.04570)

#### Manipulation
| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| CoRL 2022 | [Leveraging Language for Accelerated Learning of Tool Manipulation](https://arxiv.org/pdf/2206.13074) | - | 36 objects | images | tool utilize |

### Scene
| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| 2024 | [3D-GRAND: A Million-Scale Dataset for 3D-LLMs with Better Grounding and Less Hallucination](https://arxiv.org/pdf/2406.05132v2)| Raw | 40,087 household scenes paired with 6.2 million densely-grounded scene-language instructions | Point-cloud, text | 3D semantic segmentation  |


### Object and Scene

| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| NeurlPS 2022 | [PeRFception: Perception using Radiance Fields](https://openreview.net/pdf?id=MzaPEKHv-0J) | CO3D, ScanNet | Co3D(18669 annotated videos with a total 1.5 million of camera-annotated frames), ScanNet(1.5 K indoor scenes with commercial RGB-D sensors) | Multi-view, reconstructed Point-cloud | 2D image classification, 3D object classification, 3D semantic segmentation |

## Real and Synthetic

### Object
| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| 2023.8 | [HANDAL: A Dataset of Real-World Manipulable Object Categories with Pose Annotations, Affordances, and Reconstructions](https://arxiv.org/pdf/2308.01477v1) | videos | 308k annotated image frames from 2.2k videos of 212 real-world objects in 17 categories 3D reconstruction | reconstructed mesh | pose estimation and affordance prediction |
### Scene
| time | paper | Sources| Data Scale| Modality | Task |
|----------|----------|----------|----------|----------|----------|
| CVPR 2024 | [SceneFun3D: Fine-Grained Functionality and Affordance Understanding in 3D Scenes](https://alexdelitzas.github.io/assets/pdf/SceneFun3D.pdf) | | | | |
| 2024.1 | [SceneVerse: Scaling 3D Vision-Language Learning for Grounded Scene Understanding](https://arxiv.org/pdf/2401.09340) | ScanNet , ARKitScenes, HM3D, 3RScan, MultiScan,  Structured3D, ProcTHOR | 68K scenes and 2.5M scene-language pairs | Point cloud, scan | 3D QA |
| ECCV 2022 | [OPD: Single-view 3D Openable Part Detection](https://arxiv.org/pdf/2203.16421) | | | | |

## Scene Datasets
| time | paper | size | modality | type | source |
|----------|----------|----------|----------|----------|----------|
| 2025 | [TOD3Cap: Towards 3D Dense Captioning in Outdoor Scenes](https://arxiv.org/pdf/2403.19589) | 850 scenes | pts, Multi-view RGB | outdoor | nuScenes |
| 2024 | [SceneVerse: Scaling 3D Vision-Language Learning for Grounded Scene Understanding](https://arxiv.org/pdf/2401.09340) |  68K indoor scenes | pts | indoor | ScanNet, ARKitScenes, HM3D, 3RScan, MultiScan, RIO |
| 2024 | [EmbodiedScan: A Holistic Multi-Modal 3D Perception Suite Towards Embodied AI](https://arxiv.org/pdf/2312.16170) | 5k ego-centric RGB-D scenes | RGB-D | indoor | 3RScan, ScanNet, Matterport3D |
| 2024 | [RELLIS-3D Dataset: Data, Benchmarks and Analysis](https://arxiv.org/pdf/2011.12954) | 13,556 LiDAR scans and 6,235 images | RGB, pts | outdoor | - |
| 2024 | [SceneFun3D: Fine-Grained Functionality and Affordance Understanding in 3D Scenes](https://alexdelitzas.github.io/assets/pdf/SceneFun3D.pdf) | 710 high-fidelity 3D scenes | RGB-D(reconstructed), pts| indoor | - |
| 2023 | [Rank2Tell: A Multimodal Driving Dataset for Joint Importance Ranking and Reasoning](https://arxiv.org/pdf/2309.06597) | 116 scenes? | pts, RGB-D | outdoor | - |
| 2023 | [ScanNet++: A High-Fidelity Dataset of 3D Indoor Scenes](https://arxiv.org/pdf/2308.11417) | 460 scenes | RGB-D, pts | indoor |- |
| 2023 | [DL3DV-10K: A Large-Scale Scene Dataset for Deep Learning-based 3D Vision](https://arxiv.org/pdf/2312.16256) |  140+ RGB-D scenes; 10K+ video | Multi-view RGB; video | indoor & outdoor |- |
| 2021 | [Argoverse 2: Next Generation Datasets for Self-Driving Perception and Forecasting](https://datasets-benchmarks-proceedings.neurips.cc/paper_files/paper/2021/file/4734ba6f3de83d861c3176a6273cac6d-Paper-round2.pdf) |  20,000 sequences of unlabeled lidar point clouds and map-aligned pose | pts | outdoor | - |
| 2021 | [ARKitScenes: A Diverse Real-World Dataset For 3D Indoor Scene Understanding Using Mobile RGB-D Data](https://openreview.net/pdf?id=tjZjv_qh_CE) | 5,048 RGB-D sequences | RGB-D, pts | indoor |- |
| 2020 |[Learning 3D Semantic Scene Graphs from 3D Indoor Reconstructions](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wald_Learning_3D_Semantic_Scene_Graphs_From_3D_Indoor_Reconstructions_CVPR_2020_paper.pdf) | 1482 scenes | RGB-D | indoor |- |
| 2020 | [ScanRefer: 3D Object Localization in RGB-D Scans using Natural Language](https://daveredrum.github.io/ScanRefer/davezchen_eccv2020_scanrefer.pdf)| 800 ScanNet scenes | RGB-D | indoor |- |
| 2020 | [ReferIt3D: Neural Listeners for Fine-Grained 3D Object Identification in Real-World Scenes](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123460409.pdf) | 707 scenes with object mask | pts | indoor |- |
| 2020 | [nuScenes: A multimodal dataset for autonomous driving](https://openaccess.thecvf.com/content_CVPR_2020/papers/Caesar_nuScenes_A_Multimodal_Dataset_for_Autonomous_Driving_CVPR_2020_paper.pdf) | 1000 scenes | RGB, pts | outdoor | - |
| 2020 | [Campus3D: A Photogrammetry Point Cloud Benchmark for Hierarchical Understanding of Outdoor Scene](https://arxiv.org/pdf/2008.04968) | 937.1M points | pts | outdoor | - |
| 2012 | [Are we ready for Autonomous Driving? The KITTI Vision Benchmark Suite](https://www.cs.toronto.edu/~urtasun/publications/geiger_et_al_cvpr12.pdf) | 389 stereo and optical flow image pairs, stereo visual odometry sequences  | pts | outdoor | - |

## Statistics
! Pending
| Type \ Modality | Mesh | Point-Cloud | Multi-view | Scene-Graph |
|----------|----------|----------|----------|----------|
| Real-Object |
| Real-Scene |
| Synthetic-Object |
| Synthetic-Scene |

***

## Generative Models or Tools

### Object

### Image 2 Multi-view
- (ICLR 2024) **SyncDreamer: Generating Multiview-consistent Images from a Single-view Image** [[Paper]](https://arxiv.org/abs/2309.03453)

### Text 2 3D
- (ECCV 2024) **DreamMesh: Jointly Manipulating and Texturing Triangle Meshes for Text-to-3D Generation** [[Paper]](https://arxiv.org/pdf/2409.07454) [[Project]](https://dreammesh.github.io/), coarse-to-fine scheme
- (2022.12) **Point·E: A System for Generating 3D Point Clouds from Complex Prompts** [[Paper]](https://arxiv.org/pdf/2212.08751) 
- (2022.10) **CommonSim-1: Generating 3D Worlds** [[Project]](https://www.csm.ai/blog/commonsim-1-generating-3d-worlds), text-to-3D dynamic environment.

### Single-View 2 3D
- (CVPR 2024) **Wonder3D: Single Image to 3D using Cross-Domain Diffusion** [[Paper]](https://arxiv.org/pdf/2310.15008)
- (2024.9) **MVLLaVA: An Intelligent Agent for Unified and Flexible Novel View Synthesis** [[Paper]](https://arxiv.org/pdf/2409.07129), leveraging the power of MLLM.
- (CVPR 2024) **Splatter Image: Ultra-Fast Single-View 3D Reconstruction** [[Paper]](https://arxiv.org/pdf/2312.13150)
- (ACMM 2024) **Hi3D: Pursuing High-Resolution Image-to-3D Generation with Video Diffusion Models** [[Paper]](https://arxiv.org/pdf/2409.07452)
- (RSS 2024 Workshop) **Single-View 3D Reconstruction via SO(2)-Equivariant Gaussian Sculpting Networks** [[Paper]](https://arxiv.org/pdf/2409.07245)
- (NeurlPS 2023) **One-2-3-45: Any Single Image to 3D Mesh in 45 Seconds without Per-Shape Optimization** [[Paper]](https://arxiv.org/pdf/2306.16928)
- (CVPR 2023) **PC^2 Projection-Conditioned Point Cloud Diffusion for Single-Image 3D Reconstruction** [[Paper]](https://arxiv.org/abs/2302.10668)
- (2023.4) **Anything-3D: Towards Single-view Anything Reconstruction in the Wild** [[Paper]](https://arxiv.org/pdf/2304.10261v1)
- (ICCV 2023) **Zero-1-to-3: Zero-shot One Image to 3D Object** [[Paper]](https://arxiv.org/abs/2303.11328)


### PairedImg 2 3D
- (CVPR 2024) **pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction** [[Paper]](https://arxiv.org/pdf/2312.12337)

### Multi-View 2 3D
- (ICCV 2023) **NeuS2: Fast Learning of Neural Implicit Surfaces for Multi-view Reconstruction** [[Paper]](https://arxiv.org/pdf/2212.05231)

### Text 2 4D 
- (CVPR 2024) **Align Your Gaussians: Text-to-4D with Dynamic 3D Gaussians and Composed Diffusion Models** [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/papers/Ling_Align_Your_Gaussians_Text-to-4D_with_Dynamic_3D_Gaussians_and_Composed_CVPR_2024_paper.pdf)

### 3D part segmentation
- (CVPR 2023) **Self-positioning Point-based Transformer for Point Cloud Understanding** [[Paper]](https://arxiv.org/abs/2303.16450)
- (CVPR 2017) **PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation** [[Paper]](https://arxiv.org/abs/1612.00593) [[Code]](https://github.com/charlesq34/pointnet)
- (Proc. SGP 2023) **Cross-Shape Attention for Part Segmentation of 3D Point Clouds** [[Paper]](https://arxiv.org/abs/2003.09053) [[Code]](https://github.com/marios2019/CSN)

### 3D general model
- (ICLR 2024 Spotlight) **Uni3D: Exploring Unified 3D Representation at Scale** [[Paper]](https://arxiv.org/abs/2310.06773)
### Scene

- (2024.9) **GigaGS: Scaling up Planar-Based 3D Gaussians for Large Scene Surface Reconstruction** [[Paper]](https://arxiv.org/pdf/2409.06685) [[Project]](https://open3dvlab.github.io/GigaGS/)

### Images

#### RGB 2 Depth
- (ICCV 2021) **Vision Transformers for Dense Prediction** [[Paper]](https://openaccess.thecvf.com/content/ICCV2021/papers/Ranftl_Vision_Transformers_for_Dense_Prediction_ICCV_2021_paper.pdf)

