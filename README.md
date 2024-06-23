# ML
Lean ML


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
