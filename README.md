# ML
Lean ML

CHAPTER ONE

Provision an Azure Machine Learning workspace

Create the workspace and compute resources

In a browser, open Cloud shell in the Azure portal at https://portal.azure.com/, signing in with your Microsoft account.

In the terminal, enter the following commands to clone this repo:

```
 rm -r azure-ml-labs -f
 git clone https://github.com/MicrosoftLearning/mslearn-azure-ml.git azure-ml-labs
 ```

 After the repo has been cloned, enter the following commands to change to the folder for this lab and run the setup.sh script it contains:

```
 cd azure-ml-labs/Labs/06
 ./setup.sh
```


NOTE
""""""""
 You must have administrative access to the subcribtion. You can get details of all subscriptions


 Get the active tenant
 ```
az account tenant list

az account show
```

You can also change the active subscription

```
# change the active subscription using the subscription name
az account set --subscription "My Demos"

# change the active subscription using the subscription ID
az account set --subscription "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
```

""""""""""

When you’ve created the workspace and necessary compute resources, in the Azure portal, navigate to the Azure Machine Learning

CHAPTER TWO
In the Azure portal, navigate to the Azure Machine Learning workspace named mlw-dp100-….
Select the Azure Machine Learning workspace, and in its Overview page, select Launch studio. Another tab will open in your browser to open the Azure Machine Learning studio.
Close any pop-ups that appear in the studio.
Within the Azure Machine Learning studio, navigate to the Compute page and verify that the compute instance and cluster you created in the previous section exist. The compute instance should be running, the cluster should be idle and have 0 nodes running.

In the Compute instances tab, find your compute instance, and select the Terminal application.
On the left side, select Notebooks.

Select the Open terminal image.

In the terminal, install the Python SDK on the compute instance by running the following commands in the terminal:

```
 pip uninstall azure-ai-ml
 pip install azure-ai-ml
```
Run the following command to clone a Git repository containing notebooks, data, and other files to your workspace:
```
 git clone https://github.com/MicrosoftLearning/mslearn-azure-ml.git azure-ml-labs
```

When the command has completed, in the Files pane, click ↻ to refresh the view and verify that a new Users/your-user-name/azure-ml-labs folder has been created.

Train a classification model with automated machine learning
Now that you have all the necessary resources, you can run the notebook to configure and submit the Automated Machine Learning job.

Open the Labs/06/Classification with Automated Machine Learning.ipynb notebook.

Verify that the notebook uses the Python 3.8 - AzureML kernel.
Run all cells in the notebook.

A new job will be created in the Azure Machine Learning workspace. The job tracks the inputs defined in the job configuration, the data asset used, and the outputs like metrics to evaluate the models.

Note that the Automated Machine Learning jobs contains child jobs, which represent individual models that have been trained and other tasks needed to execute.

Go to Jobs and select the auto-ml-class-dev experiment.
Select the job under the Display name column.
Wait for its status to change to Completed.


