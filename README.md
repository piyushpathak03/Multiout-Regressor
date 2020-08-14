# Multiout-Regressor

[![Documentation Status](https://readthedocs.org/projects/amorf/badge/?version=latest)](https://amorf.readthedocs.io/en/latest/?badge=latest) 
[![PyPI version shields.io](https://img.shields.io/pypi/v/amorf.svg)](https://pypi.org/project/amorf/) 
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/amorf.svg)](https://pypi.python.org/pypi/ansicolortags/)

# amorf - A Multi-Output Regression Framework


amorf is a Python library for multi-output regression. It combines several different approaches to help you get started with multi-output regression analyisis. 

## Motivation 
Multi-output (or multi-target) regression models are models with multiple continous target variables. 

The idea of this framework/library is to collect and combine several different apporaches for multi-output regression in one place. This allows you to get started real quick and then extend and tweak the provided models to suit your needs.
## Getting Started 

[//]: # (### Prerequisites )

### Installation 

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install amorf.

```bash
pip install amorf
```
### Usage 
```python
import amorf.neuralNetRegression as nnr 
from amorf.metrics import average_relative_root_mean_squared_error as arrmse

# for data generation
from sklearn.datasets import make_regression
from sklearn.model_selection import train_test_split

X, y = make_regression(n_samples=10000, n_features=12, n_targets=3, noise=0.1) 
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

regressor = nnr.NeuralNetRegressor(patience=5, training_limit=None) #initialize neural net regressor
regressor.fit(X_train, y_train) #fit regressor to training data
prediction = regressor.predict(X_test) #predict test data 
print(arrmse(prediction, y_test)) #print error
```

## Running The Tests 
Clone repository

```bash 
git clone https://github.com/piyushpathak03/Multiout-Regressor/
```
Change directory 
```bash 
cd amorf/
``` 
Disocver and run tests 

```bash 
python -m unittest discover -s tests -p 'test_*.py'
```


## About me

**Piyush Pathak**

[**PORTFOLIO**](https://anirudhrapathak3.wixsite.com/piyush)

[**GITHUB**](https://github.com/piyushpathak03)

[**BLOG**](https://medium.com/@piyushpathak03)


# 📫 Follw me: 

[![Linkedin Badge](https://img.shields.io/badge/-PiyushPathak-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/piyushpathak03/)](https://www.linkedin.com/in/piyushpathak03/)

<p  align="right"><img height="100" src = "https://media.giphy.com/media/l3URDstnIjBNY7rwLB/giphy.gif"></p>
