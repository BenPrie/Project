# Practical Quantum Algorithms for Cryptanalysis

This contains all implementation and experimentation work for my Honour's project. Here is a brief contents to help you navigate if you so wish:

I do all of my work through notebooks:

- `Defining the SQIF.ipynb` walks through the SQIF algorithm in [Yan et al. (2022)](https://arxiv.org/abs/2212.12372) step-by-step. It proceeds right the way up to the linear system of equations that one solves to reveal factors, though does not do this because (1) that is not what we care about in this project, and (2) we agree with [Grebnev et al. (2023)](https://arxiv.org/html/2303.04656v6) that there are cases for which not enough sr-pairs can be found to successfully factor (and give the example).
- `Building a Hamiltonian.ipynb` concisely presents the implementation of our code that derives a Hamiltonian for a given semi-prime and hyperparameters. There is no walkthrough -- this is given elsewhere.
- `CVP Solutions to Factors.ipynb` is an early-stage working notebook that I used in understanding the post-sieving working of the algorithm. Again, we are not actually all that interested in this, I just wanted to make it clear to myself.
- `Replicating Yan et al. (2022).ipynb` gives a detailed walkthrough of our implementation of [Yan et al. (2022)](https://arxiv.org/abs/2212.12372)'s method, including the full derivation of the Hamiltonian.
- `Sampling by QAOA.ipynb` walks through the process of sampling solutions by measuring the output states of the QAOA circuit.
- `Experiments.ipynb` looks at the sampled solutions our implementation obtains for the cases used in [Yan et al. (2022)](https://arxiv.org/abs/2212.12372).
- `VQA for CVP.ipynb` contains all of our data generation and data analysis. Most of our findings and novel contributions appear in this notebook.

For ease-of-use, notebook work is sometimes cleanly collected into scripts to be called on later:

- `sqif.py` packages all of the functionality for our implementation of the SQIF algorithm (focusing on the CVP subroutine, not the full factoring).