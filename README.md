# Distributed-Regression-Network-DRN-

**Distribhution Regression Network (DRN)** is a generalized Multilayer Perceptron (MLP) that performs regression from input probability distribution to output probability distribution. Performing regression on regression has many applications, such as studying of human population, modeling phenotypic traits evolution and meteorological phenomenon. Traditional methods break down distribution into discrete values or basis function approximation (e.g. Triple Basis Rstimator (3BE)) and feed each values into **multiple** input nodes in a MLP. DRN encodes one entire distribution/function in one **single** node in MLP

DRN is inspired by Boltzmann distribution, which is a probability distribution used in statistical mechanics that describes the distribution of energy states of a system in thermal equilibrium. DRN is tested with Ornstein-Uhlenbeck (OU) process which is a mean-reverting random-walk behavior describing Brownian motion with friction. DRN is also applied to stock data and cell data, which tend to revert into stable state over time. Result below shows that DRN **performs better** than 3BE and typical Multilayer Perceptron (MLP) with **less number of parameters**.

_________________________________________________ <br />
| Model |  L2 test loss   | Number of Parameter | <br />
|-------+-----------------+---------------------| <br />
|  DRN  | 0.1441 ± 0.0010 |         5           | <br />
|  MLP  | 0.1475 ± 0.0005 |        703          | <br />
|  3BE  | 0.1255 ± 0.0083 |        272          | <br />
|_______|_________________|_____________________| <br />
Table shows comparison of L2 test loss and the number of model parameters used for the Ornstein-Uhlenbeck (OU) data. 

______________________________________________________________ <br />
| Model |  Log-likelihood on test set   | Number of Parameter | <br />
|-------+-------------------------------+---------------------| <br />
|  DRN  |        474.43 ± 0.01          |         7           | <br />
|  MLP  |        471.50 ± 0.08          |        4110         | <br />
|  3BE  |        466.76 ± 0.73          |        8100         | <br />
|______ | _____________________________ | ____________________| <br />
Table shows comparison of log-likelihood on the stock data and the number of model parameters.               
