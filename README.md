# dscc202-402-spring2024
Course materials for DSCC-202-402
## Establishing a GitHub account if you do not have one already
[Sign up for a new github account](https://docs.github.com/en/github/getting-started-with-github/signing-up-for-a-new-github-account) <br>

## Fork the class repository into your account
Could you unlock the dsc402 repository into your new account?  Note: this will create a copy of the course repo for you to add and work on within your
own account.<br>
Go to https://github.com/lpalum/dscc202-402-spring2024 and hit the fork button while you are logged into your GitHub account: ![fork image](https://github-images.s3.amazonaws.com/help/bootcamp/Bootcamp-Fork.png)

## Clone your copy of the dsc402 repository to get the class materials on your machine
<code>git clone https://github.com/[your account name]/dscc202-402-spring2023.git</code><br>
note: you may want to clone this repo into a directory on your machine that you organize for code e.g. **/home/<your username>/code/github**

Note: **/home/[your account name] should be /Users/[your account name] to work with the paths that are defined in Mac OS X.**

## Sign up for the Community Edition of Databricks and import archives
[Databrick Community Edition](https://www.databricks.com/try-databricks#account)
<table>
<tr>
<td><img src="https://data-science-at-scale.s3.amazonaws.com/images/dbce1.png"></td>
<td><img src="https://data-science-at-scale.s3.amazonaws.com/images/dbce2.png"></td>
<td><img src="https://data-science-at-scale.s3.amazonaws.com/images/dbce3.png"></td>
</tr>
<table>
<h2>NOTES:</h2>
<ul>
<li>THE SELECTION OF THE DATABRICKS COMMUNITY EDITION LINK AT THE BOTTOM OF THE FORM... DO NOT SIGN UP FOR THE FULL VERSION!
<li>You will also receive an invite later in the course to the class-shared Databricks Workspace, where you will be doing your final project.
</ul>

Here is some helpful information about importing archives into the Databricks Environment: 
https://docs.databricks.com/notebooks/notebooks-manage.html#import-a-notebook

Import the DBC archive into your account from the Learning Spark v2 GitHub repository. (this is the code that goes along with the test book)
[DBC Archive](https://github.com/databricks/LearningSparkV2/blob/master/notebooks/LearningSparkv2.dbc)

Import the DBC archives for the class after unzipping dscc202-402-dbc.zip on your machine.
- asp.dbc   apache spark programming
- de.dbc    data engineering with delta lake and spark
- ml.dbc    machine learning on spark

## Running your own local Spark Environment on your Computer [optional]
[Install docker on your computer](https://docs.docker.com/get-docker/)

Pull the all-spark-notebook image from docker hub: <br>
<code>https://hub.docker.com/r/lpalum/dsc402</code>
<br>Launch the docker image to open a Jupyter Lab instance in your local browser:<br>
<code>docker run -it --rm -p 8888:8888 --name all-spark --volume /home/[your account name]/code/github:/home/jovyan/work lpalum/dsc402 start.sh Jupyter lab</code>

This will start a Jupyter lab instance on your machine that you will be able to access at port 8888 in your browser, and it will mount the GitHub repo that you previously
cloned into the container working directory.
