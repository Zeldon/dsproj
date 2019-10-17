dsproj
==============================

Template for a standard DS project. With some customizations.


## Initializations

### 1. Environment
- [ ] <small>Do remember to switch to correct git remote.</small>  

- [ ] Environment is through [virtualenv](https://virtualenv.pypa.io/en/latest/) and [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/).  
Initialize after pip installs as such:  

        pip install virtualenv
        pip install virtualenvwrapper

        $ export WORKON_HOME=~/Envs
        $ mkdir -p $WORKON_HOME
        $ source /usr/local/bin/virtualenvwrapper.sh


    Then...

        mkvirtualenv env1


- [ ] Then proceed with requirements install...  
Its better to install requirements via makefile: `make requirements`  
This essentially executes steps:  

    `pip install -U pip setuptools wheel`  
    `pip install -r base_requirements.txt` 

TODO:  
(This actually installs a ton of requirements so <u>refresh and use own requirements</u>.)


### 2. Key Notes

- [ ] Data folder is delibrately not excluded from gitignore to show flow of folder structures.
We should self add data files that should not be included once project has been setup.  


### 3. Template
<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>.</small></p>  

`pip install cookiecutter`  

`cookiecutter https://github.com/drivendata/cookiecutter-data-science`

**Base Requirements.txt**  
- click
- Sphinx
- coverage
- awscli
- flake8
- python-dotenv>=0.5.1

---


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.testrun.org


--------

