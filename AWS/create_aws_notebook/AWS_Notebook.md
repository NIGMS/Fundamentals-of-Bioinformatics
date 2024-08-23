# Using SageMaker Notebooks

AWS offers different types of Notebook instances: SageMaker Studio, SageMaker Notebook Instances, and SageMaker Studio Lab. SageMaker Notebook Instances offer the most flexibility in terms of installing local software via conda/mamba or launching from custom containers. [SageMaker Studio](https://docs.aws.amazon.com/sagemaker/latest/dg/studio.html) and [SageMaker Studio Lab](https://aws.amazon.com/sagemaker/studio-lab/) allow for 'on the fly' machine resizing and notebook scheduling, as well as not worrying about resource availability, but they run in a managed environment and offer less flexibility for installing custom software. Most machine-learning related software are pre-installed, but these can be hard to use for a lot of bioinformatic tasks where you need to install CLI tools with conda.

### Set up a SageMaker Notebook Instance

1. In AWS console, type **Amazon SageMaker** in search bar and click it:

  ![selectsagemaker](Screenshot1.png)

2. On the left side bar click **Notebooks**:

  ![Notebooks](Screenshot2.png)

3. Click **Create notebook instance**:

  ![create_new_notebook](Screenshot3.png)

4. Give a name to your notebook. Choose **ml.m5.xlarge** as notebook instance type and Amazon Linux 2 as platform identifier:

    ![environment](Screenshot4.png)
   
5. It will take about 5 minutes, your notebook instance to get ready:

    ![pending](Screenshot5.png)
   
6. **Open Jupyter Lab**:

    ![jupyterlab](Screenshot6.png)

7. Upload your jupyter notebook

  ![upload](Screenshot7.png)

8. Select the kernel:

  ![kernel](Screenshot8.png)

9. **IMPORTANT**: **Stop** the kernel at end of your work to avoid getting charged.

    ![resize image](Screenshot9.png)