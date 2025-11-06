# conditional_diffusion_inverse_prediction
[![python](https://img.shields.io/badge/python-v3.9.17-blue)](https://www.python.org/downloads/release/python-3917/)

This repository contains the code for a conditional diffusion model used to perform inverse analysis in the materials field.
Specifically, we perform inverse analysis to propose microstructures and process parameters that satisfy the desired material properties.
This inverse analysis has the potential to reduce the costs associated with trial-and-error experimentation and simulation in materials development, and contribute to greater efficiency.
In this case, we propose a model that suggests the microstructure and processing temperature to achieve the desired elastic modulus for thermoplastic resins as an example. However, it can be easily applied to other materials, material properties, and process parameters by replacing the dataset. Furthermore, it can be easily extended to handle multiple process parameters.

## File discription
```training.ipynb``` : The code for performing training. Save the trained model.

```modelload.ipynb``` : Load the saved model and perform generation.

```modules.py``` : This program includes models such as U-Net. Import this file when running ```training.ipynb``` or ```modelload.ipynb```.

## Datasets discription
This program uses a dataset located in the ```train_val_test``` directory.
The dataset consists of microstructure images (.vtk) and their corresponding elastic properties (.out).

- The microstructure images were generated using the phase-field method, then compressed for model training.

- The elastic properties were computed using the XFEM-based computational micromechanics approach.

The methodologies used to generate these datasets are based on the following research works:
```
Higuchi, R. et al. (2022). Multiphysics simulation of cooling-rate-dependent material properties of thermoplastic composites. Proc. 20th European Conference on Composite Materials (ECCM20).
```
```
Takashima, R., Higuchi, R., Oshima, S., Yokozeki, T. & Aoki, T. (2024). Prediction of mechanical properties of thermoplastic resins considering molding conditions. Proc. 21st European Conference on Composite Materials (ECCM21).
```
```
Higuchi, R., Okabe, T. & Nagashima, T. (2017). Numerical simulation of progressive damage and failure in composite laminates using XFEM/CZM coupled approach. Composites Part A: Applied Science and Manufacturing, 95, 197–207. https://doi.org/10.1016/j.compositesa.2016.12.026.
```
```
Higuchi, R., Yokozeki, T., Nagashima, T. & Aoki, T. (2019) Evaluation of mechanical properties of noncircular carbon fiber reinforced plastics by using XFEM-based computational micromechanics. Composites Part A: Applied Science and Manufacturing, 126, 105556. https://doi.org/10.1016/j.compositesa.2019.105556.
```

## Usage
First, clone this repository to your local machine.
```sh
git clone https://github.com/mmc-research-group/conditional_diffusion_inverse_prediction.git
```

## Citation
If you use this repository, please cite:
```
IIkeda, A., Higuchi, R., Yokozeki, T., Endo, K., Kojima, Y., Suzuki, M., & Muramatsu, M. (2025). Conditional diffusion model for inverse prediction of process parameters and dendritic microstructures from mechanical properties. Scientific Reports, 15(1), 37147. https://doi.org/10.1038/s41598-025-22942-y.
```

In Bibtex format
```
@article{ikeda2025conditional,
  title={Conditional diffusion model for inverse prediction of process parameters and dendritic microstructures from mechanical properties},
  author={Ikeda, Arisa and Higuchi, Ryo and Yokozeki, Tomohiro and Endo, Katsuhiro and Kojima, Yuta and Suzuki, Misato and Muramatsu, Mayu},
  journal={Scientific Reports},
  volume={15},
  number={1},
  pages={37147},
  year={2025},
  publisher={Nature Publishing Group UK London}
}
```

## References & Acknowledgements
Our implementation builds upon and acknowledges the following open-source project and foundational research:
- Diffusion Models in PyTorch by dome272 and tcapelle. https://github.com/tcapelle/Diffusion-Models-pytorch.
```
Ho, J., Jain, A., & Abbeel, P. (2020). Denoising Diffusion Probabilistic Models. arXiv:2006.11239. https://doi.org/10.48550/arXiv.2006.11239.
```

## Lisence
This project is licensed under the MIT LICENSE - see the [LICENSE.txt](LICENSE.txt) file for details
