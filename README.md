# Data Engineering with Snowpark

### ➡️ For more complete instructions please check out the new [Data Engineering Pipelines with Snowpark Python](https://quickstarts.snowflake.com/guide/data_engineering_pipelines_with_snowpark_python/index.html?index=..%2F..index#0) Quickstart.

<br /><br />
This repository contains a hands-on lab for data engineering in Snowflake with Snowpark! Here is an overview of what we'll build in this lab:

<img src="images/demo_overview.png" width=800px>

## Preview Features
Note: The following features/tools used in this lab are still in preview
* [Snowflake Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=snowflake.snowflake-vsc)
* [snowcli](https://github.com/Snowflake-Labs/snowcli)


# Setup
You will need the following things before beginning:

* Snowflake
    * **A Snowflake Account**
    * **A Snowflake user created with ACCOUNTADMIN permissions**. This user will be used to get things setup in Snowflake.
* Anaconda
    * **Anaconda installed on your computer**. Check out the [Anaconda Installation](https://docs.anaconda.com/anaconda/install/) instructions for the details.
* SnowSQL
    * **SnowSQL installed on your computer**. Go to the [SnowSQL Download page](https://developers.snowflake.com/snowsql/) and see the [Installing SnowSQL](https://docs.snowflake.com/en/user-guide/snowsql-install-config.html) page for more details.
    * Create a SnowSQL configuration for this lab by adding the following section to your `~/.snowsql/config` file (replacing the account, username, and password with your values):
    * **Note:** this will not work with key pair at this time, these are the required parameters for [utils/snowpark_utils.py](utils/snowpark_utils.py)

        ```
        [connections.dev]
        account = myaccount
        username = myusername
        password = mypassword
        rolename = HOL_ROLE
        warehousename = HOL_WH
        dbname = HOL_DB
        ```
* Visual Studio Code with required extensions
    * **Visual Studio Code installed on your computer**. Check out the [Visual Studio Code](https://code.visualstudio.com/) homepage for a link to the download page.
    * **Python extension installed**. Search for and install the "Python" extension in the *Extensions* pane in VS Code.
    * **Snowflake extension installed**. Search for and install the "Snowflake" extension in the *Extensions* pane in VS Code.
* GitHub account with lab repository forked and cloned locally
    * **A GitHub account**. If you don't already have a GitHub account you can create one for free. Visit the [Join GitHub](https://github.com/signup) page to get started.
    * **A forked lab repository**. You'll need to create a fork of this lab repository in your GitHub account. Visit the [tko-data-engineering GitHub Repository](https://github.com/sfc-gh-jhansen/tko-data-engineering) and click on the "Fork" button near the top right. Complete any required fields and click "Create Fork".
    * **A local clone of the forked lab repository**. For connection details about your Git repository, open the Repository and copy the "HTTPS" link provided near the top of the page. If you have at least one file in your repository then click on the green "Code" icon near the top of the page and copy the "HTTPS" link. Use that link in VS Code to clone the repo to your computer. Please follow the instructions at [Clone and use a GitHub repository in Visual Studio Code](https://learn.microsoft.com/en-us/azure/developer/javascript/how-to/with-visual-studio-code/clone-github-repository) for more details.
* Anaconda environment
    * Create a conda environment for this lab using the supplied `conda_env.yml` file. Run these commands from a terminal in the root of your local repository.

        ```bash
        conda env create -f conda_env.yml
        ```

# Running the Demo
Here are a few tips/ticks for running the demo; which is run from the QuickStart linked above:

* For each Python step, run the script through a terminal
    * For best results, open a terminal in VS Code
    * Activate your Conda environment with `conda activate pysnowpark`
    * Change directory to the folder containing the script you want to run (using `cd` in the terminal)
    * Then run the script with `python <script-name>.py`
* Don't try and run the Python script through the VS Code debugger as some paths will get messed up.
    * This includes both from the VS Code editor's debug menu (`Run Python File` or `Debug Python File`) and from the Debugger extension.
