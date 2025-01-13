# 3D Gaussian Splatting Project
This **Temporal 3D Reconstruction of Cultural Heritage using Gaussian Splatting** focuses on leveraging advanced Gaussian Splatting (GS) techniques to model and visualize temporal changes in cultural heritage sites. The objective is to capture and highlight transformations caused by natural degradation or environmental factors over time. Through innovative visualization techniques, the project aims to create a "time capsule" model that preserves and analyzes these sites, contributing to their long-term digital preservation.

### Model Processing

We explored three methods for merging 3D models: **CloudCompare**, **MeshLab**, and a custom **Python** solution. All methods rely on the **Iterative Closest Point (ICP)** algorithm or on the **Point Pairs Picking **, which aligns models by minimizing the distance between corresponding points.

#### CloudCompare
CloudCompare was used to align and merge two PLY models: one intact and one simulating damage. Two alignment methods were tested:
1. **ICP**: Automated alignment using iterative point distance reduction.
2. **Point Pairs Picking**: Manual selection of matching points for alignment.

After alignment, the models were merged into a single exportable file.

![Initial Configuration](images/CloudeCompare/statues_for_icp_cloude_compare.jpg)  
*Initial configuration of models.*

![Merged Models](images/CloudeCompare/alignment_differences_cloude_compare.jpg)  
*Merged models with highlighted differences.*

#### MeshLab
MeshLab, developed by ISTI-CNR, was also tested but proved less effective. Its ICP implementation requires manual point pairing, leading to higher error rates and reduced reliability.

![Point Pairs Picking](images/meshlab/satiroebaccante_icp_meshlab2.png)  
*Manual point pairing in MeshLab.*

![Aligned Models](images/meshlab/satiroebaccante_merging_meshalb2.png)  
*Models after ICP alignment in MeshLab.*

#### Python Implementation
A custom Python solution was developed for greater flexibility and precision. Key steps included:
1. **Data Loading**: Extracting coordinates and colors from PLY files.
2. **ICP Registration**: Aligning models using the ICP algorithm.
3. **Difference Visualization**: Highlighting changes (erosion or new material) using a KDTree structure.
4. **PLY Reconstruction**: Exporting the merged model for interactive visualization.

![Before ICP](images/coding/Code_ICP_Before.png)  
*Models before ICP alignment.*

![After ICP](images/coding/Code_ICP_After.png)  
*Models after ICP alignment.*

![Differences](images/coding/Code_Broken3.png)  
*Highlighted differences between models.*

# Collaborators

This project was developed by:

- [@Martin-Martuccio](https://github.com/Martin-Martuccio) - Martin Martuccio
  
- [@PSamK](https://github.com/PSamK) - Samuele Pellegrini
  
- [@biaperass](https://github.com/biaperass) - Bianca Perasso
  
- [@LorenzoMesi](https://github.com/LorenzoMesi) - Lorenzo Mesi
  
## Contact

For questions, issues, or collaborations, please contact:

- Martin Martuccio: [[martinmartuccio@gmail.com](Martin:martinmartuccio@gmail.com)]

- Samuele Pellegrini: [[pellegrini.samuele.1@gmail.com](Samuele:pellegrini.samuele.1@gmail.com)]

- Bianca Perasso: [[bianca.perasso@gmail.com](Bianca:bianca.perasso@gmail.com)]

- Lorenzo Mesi: [[mesilorenzo@gmail.com](Lorenzo:mesilorenzo@gmail.com)]

## Acknoledgements

This project was developed to explore the potential of Gaussian Splatting techniques for cultural heritage preservation, as part of the project exam for the course [Augmented and Virtual Reality](https://corsi.unige.it/off.f/2023/ins/66562) during Master's degree in Computer Engineering - Artifical Intelligence at the University of Genova.

# License

This project is licensed under the MIT License. See the `LICENSE` file for details.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python: 3.11](https://img.shields.io/badge/Python-3.11-blue.svg)

