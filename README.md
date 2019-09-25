# PySpark AWS EMR
## Prerequisites
- NLTK
- Tensorflow
- Tensorflow-hub
- Numpy
- Anaconda
## Setting up AWS EMR
This code was run using a mater node (m5.2xlarge) and 2 slaves (m4.2xlarge). configration is included in `config.json` and boostrap script is included in `bootstrap.sh`. Modules used in EMR are:
- Hadoop 2.8.5
- Spark 2.4
- Livy 0.5.0
- Tensorflow 1.12.0

## Installing Anaconda
To intsall anaconda run the following commands
```
wget https://repo.continuum.io/archive/Anaconda3-5.2.0-Linux-x86_64.sh
bash Anaconda3-5.2.0-Linux-x86_64.sh
```
Next, add the following lines to `~/.bashrc`
```
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook --no-browser --port=8888 --ip=0.0.0.0'
```
Then run the following line:
```
source ~/.bashrc
```
## Installing tensorflow and tensorflow-hub into anaconda env
First, change current env using the following code:
```
source activate base
```
Then, install using pip
```
pip install tensorflow
pip install tensorflow-hub
```
## Running EMR notebook
When you have satisfyied all the above steps, run `pyspark` command and connect to emr notebook using EMR master public DNS (make sure to enable port 8888 in inboud traffic)
## Running spark jobs
All code to run spark jobs are inside `Assignment_2.ipynb`

