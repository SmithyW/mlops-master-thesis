# mlops-master-thesis

## Getting started

_This getting started guide is written for Linux systems. During development, an Ubuntu 24.04 and Debian 12.6 were used.
MacOS is not tested but should also work._

### General setup

Create a virtual environment (e.g. python3.12)

`python -m venv <virtual environment>`

Enter the virtual environment

`source <virtual environment>/bin/activate`

Install all required python packages using

`pip install -r requirements.txt`

### Data version control

TODO: S3 cloud storage instead of local server 

Data has to be stored and managed in the `data` directory. After changing a file the follwing commands should be executed:

`dvc add data/<edited file>`

`git commit data/<edited file>.dvc -m "Dataset updated"`

`dvc push`

