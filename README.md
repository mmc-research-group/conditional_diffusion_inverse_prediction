# conditional_diffusion_inverse_prediction
[![python](https://img.shields.io/badge/python-v3.9.17-blue)](https://www.python.org/downloads/release/python-3917/)

This repository contains the code for a conditional diffusion model used to perform inverse analysis in the materials field.
Specifically, we perform inverse analysis to propose microstructures and process parameters that satisfy the desired material properties.
This inverse analysis has the potential to reduce the costs associated with trial-and-error experimentation and simulation in materials development, and contribute to greater efficiency.
In this case, we propose a model that suggests the microstructure and processing temperature to achieve the desired elastic modulus for thermoplastic resins as an example. However, it can be easily applied to other materials, material properties, and process parameters by replacing the dataset. Furthermore, it can be easily extended to handle multiple process parameters.

## File discreption
```training.ipynb``` : The code for performing training. Save the trained model.

```modelload.ipynb``` : Load the saved model and perform generation.

```modules.py``` : This program includes models such as U-Net. Import this file when running ```training.ipynb``` or ```modelload.ipynb```.

## Usage
First, clone this repository to your local machine.
```sh
git clone https://github.com/mmc-research-group/conditional_diffusion_inverse_prediction.git
```

## Citation
If you use this repository, please cite:
```sh
Ikeda, A., Higuchi, R., Yokozeki, T., Endo, K., Kojima, Y., Suzuki, M., & Muramatsu, M. (2025). Conditional diffusion model for inverse prediction of process parameters and dendritic microstructures from mechanical properties. Scientific Reports, 15(1), 37147.
https://doi.org/10.1038/s41598-025-22942-y
```

In Bibtex format
```sh
@article{ikeda2025conditionaldiffusionmodelinverse,
  title={Conditional diffusion model for inverse prediction of process parameters and dendritic microstructures from mechanical properties},
  author={Ikeda, Arisa and Higuchi, Ryo and Yokozeki, Tomohiro and Endo, Katsuhiro and Kojima, Yuta and Suzuki, Misato and Muramatsu, Mayu},
  journal={arXiv preprint arXiv:2410.20822},
  year={2025}
}
```

## References & Acknowledgements
Our implementation builds upon and acknowledges the following open-source project and foundational research:
- Diffusion Models in PyTorch by dome272 and tcapelle
[https://github.com/tcapelle/Diffusion-Models-pytorch](https://github.com/tcapelle/Diffusion-Models-pytorch)
- Ho, J., Jain, A., & Abbeel, P. (2020). Denoising Diffusion Probabilistic Models. arXiv:2006.11239.
[https://doi.org/10.48550/arXiv.2006.11239](https://doi.org/10.48550/arXiv.2006.11239)

## Lisence
This project is licensed under the MIT LICENSE - see the [LICENSE.txt](LICENSE.txt) file for details
