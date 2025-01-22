# ARCTICA: mAchine leaRning for Constrained-based meTabolIc Control Analysis

Accompanying code to [Machine learning predicts system-wide metabolic flux control in cyanobacteria](https://www.sciencedirect.com/science/article/pii/S1096717624000296).

ARCTICA applies a comparative flux sampling analysis as a guide for strain design. It consists of three steps:

(i)	Implementation of flux balance analysis to compute the maximal production rate of the metabolite of interest. Then, the excretion rate of the selected metabolite is constrained to 10% and 90% of the predicted maximal production rate to yield two metabolic reconstructions, representing high-producing and low-producing strains (virtual phenotypes).

(ii) Application of Monte Carlo random flux sampling on the two newly-generated metabolic reconstructions to compute the probability of all feasible fluxes that satisfy the network constraints.

(iii) Generation of a comprehensive data matrix by concatenating the obtained datasets from step ii to be employed as input features (metabolic fluxes) for training the machine learning model. 
Thereafter, using logistic regression for feature selection and extracting feature importance score, metabolic reactions that statistically influence and distinguish the two virtual phenotypes are mined and ranked.

### Python package versions:

* Python 3.10.12
* Pickle 4.0
* Numpy 1.23.5
* Pandas 1.5.3
* Matplotlib 3.7.1
* Seaborn 0.12.2
* Scipy 1.7.3
* Scikit-learn 1.2.2
* COBRApy 0.20.0
