# 3D Gaussian Splatting Project
This **Temporal 3D Reconstruction of Cultural Heritage using Gaussian Splatting** focuses on leveraging advanced Gaussian Splatting (GS) techniques to model and visualize temporal changes in cultural heritage sites. The objective is to capture and highlight transformations caused by natural degradation or environmental factors over time. Through innovative visualization techniques, the project aims to create a "time capsule" model that preserves and analyzes these sites, contributing to their long-term digital preservation.

### Model Processing

For merging 3D models, we explored three different methods: **CloudCompare**, **MeshLab**, and a custom **Python** solution. All methods are based on the **Iterative Closest Point (ICP)** algorithm or the **Point Pairs Picking technique**, which align models by iteratively minimizing the distance between corresponding points. Below are the dedicated repositories for each method:
- [**CloudCompare**](https://github.com/LorenzoMesi/AVR-CloudCompare): This repository contains instructions for using CloudCompare to align and merge 3D models.
- [**MeshLab**](https://github.com/biaperass/ICP_Merging_Meshlab): Detailed steps and documentation for performing model merging using MeshLab are available in this repository.
- [**Coding**](https://github.com/Martin-Martuccio/ICP-Merging): This repository includes a custom Python implementation of the ICP algorithm using the Open3D library, allowing automated alignment and merging of 3D models.

#### CloudCompare
CloudCompare was used to align and merge two PLY models: one intact and one simulating damage. Two alignment methods were tested:
1. **ICP**: Automated alignment using iterative point distance reduction.
2. **Point Pairs Picking**: Manual selection of matching points for alignment.

After alignment, the models were merged into a single exportable file.

![Initial Configuration](docs/images/cloudcompare/statues_for_icp.jpg)  
*Initial configuration of models.*

![Merged Models](docs/images/cloudcompare/alignment_differences.jpg)  
*Merged models with highlighted differences.*

#### MeshLab
MeshLab, developed by ISTI-CNR, was also tested but proved less effective. Its ICP implementation requires manual point pairing, leading to higher error rates and reduced reliability.

![Point Pairs Picking](docs/images/meshlab/satiroebaccante_icp_meshlab.png)  
*Manual point pairing in MeshLab.*

![Aligned Models](docs/images/meshlab/satiroebaccante_merging_meshalb.png)  
*Models after ICP alignment in MeshLab.*

#### Python Implementation
A custom Python solution was developed for greater flexibility and precision. Key steps included:
1. **Data Loading**: Extracting coordinates and colors from PLY files.
2. **ICP Registration**: Aligning models using the ICP algorithm.
3. **Difference Visualization**: Highlighting changes (erosion or new material) using a KDTree structure.
4. **PLY Reconstruction**: Exporting the merged model for interactive visualization.

![Before ICP](docs/images/coding/Code_ICP_Before.png)  
*Models before ICP alignment.*

![After ICP](docs/images/coding/Code_ICP_After.png)  
*Models after ICP alignment.*

![Differences](docs/images/coding/Code_Broken3.png)  
*Highlighted differences between models.*

# Collaborators

This project was developed by:

- [@Martin-Martuccio](https://github.com/Martin-Martuccio) - Martin Martuccio
  
- [@PSamK](https://github.com/PSamK) - Samuele Pellegrini
  
- [@biaperass](https://github.com/biaperass) - Bianca Perasso
  
- [@LorenzoMesi](https://github.com/LorenzoMesi) - Lorenzo Mesi
  
## Contact

For questions, issues, or collaborations, please contact:

- Martin Martuccio: [martinmartuccio@gmail.com](Martin:martinmartuccio@gmail.com)

- Samuele Pellegrini: [pellegrini.samuele.1@gmail.com](Samuele:pellegrini.samuele.1@gmail.com)

- Bianca Perasso: [bianca.perasso@gmail.com](Bianca:bianca.perasso@gmail.com)

- Lorenzo Mesi: [mesilorenzo@gmail.com](Lorenzo:mesilorenzo@gmail.com)

## Acknoledgements

This project was developed to explore the potential of Gaussian Splatting techniques for cultural heritage preservation, as part of the project exam for the course [Augmented and Virtual Reality](https://corsi.unige.it/off.f/2023/ins/66562) during Master's degree in Computer Engineering - Artifical Intelligence at the University of Genova.

# License

This project is licensed under the MIT License. See the `LICENSE` file for details.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python: 3.11](https://img.shields.io/badge/Python-3.11-blue.svg)

