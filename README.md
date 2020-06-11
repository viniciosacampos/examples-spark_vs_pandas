![json](images/pandas.png)
![json](images/vs.png)
![json](images/spark.png)

## Test of performance of compare with big two frameworks to transformer and process data very used by companies. These frameworks are Spark X Pandas and them using the same file and rules for processing.

## Start

  Above you have to step by step how install and execute test the program.

## Requirements

#### Install Docker

  Docker framework is necessary for running tests if you don't have above has a link with instructions.

* [Docker](https://docs.docker.com/engine/install/)

#### Image Docker
  
  Above we are link to download that has image docker with Spark and Pandas and this image has a framework Jupyter it is used for data scientists.  

* [Image Docker](https://hub.docker.com/r/jupyter/all-spark-notebook/)

#### Jupyter

  If you know more about this Jupyter then follow the link bellow.

* [Jupyter](https://jupyter.org/)

#### Download project 

  We need download the project of the github because we are using the objects for create the volume in the container.

* [GitHub](https://github.com/viniciosacampos/spark_vs_pandas/archive/master.zip)


#### Docker

  Now we are create repository where put our project.

```
mkdir ~/docker/volume
```

  Moving project to folder that created before.

```
mv ~/Downloads/spark_vs_pandas/* ~/docker/volume/
```

  For check installation docker run command above

```
docker --version
```

  Let's go now run our image for create the container with framework Spark and Pandas. You need put the same directory that created before and with this command the file mirror inside the container.

```
docker run -p 8888:8888 -v ~/docker/volume:/home/jovyan/work/ jupyter/all-spark-notebook
```

## Tests

All files .ipynb have instructions inside.

You can fell free for change the logical or another tests with size the file.

Let's start!

The file that we moved before has a directory structure *artifacts/data/input* where the file .csv will be written and *artifacts/data/output* where the program saved the files in parquet.

The POC have three files in .ipynb where the first step we will create the file .csv, for good test you can put number the lines that will be created in the file I recommend **20000000** million of lines

The second step you can run etl_pandas, but you need put the number of lines that you created with .csv before.

The third step you run etl_spark and put the same number of lines for test.

The final execution of the three steps you can feel the diference of processing that's frameworks but of course that not exists right or wrong, everything of necessity and size the files.

I hope you like it!