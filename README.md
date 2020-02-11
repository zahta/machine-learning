---
#### :four_leaf_clover: I am studying *Data science*. In this repository, I am going to write about my experiences in studying *Machine learning*, with a step by step approach. :four_leaf_clover:
---

### :star: Anaconda
   - [Installation](https://docs.anaconda.com/anaconda/install/)
     - [Installing on Windows](https://docs.anaconda.com/anaconda/install/windows/)
       - I had an issue with Anaconda installation on windows 7, `Failed to create Anaconda menus`. With the help of an [answer](https://stackoverflow.com/a/57635204/12777699) from <a href="https://stackoverflow.com/questions/tagged/python"><img  src=https://upload.wikimedia.org/wikipedia/commons/f/f7/Stack_Overflow_logo.png width="90"/>
</a>, version 2019.03 of Anaconda (from [download archive](https://repo.continuum.io/archive/)) successfully installed.
   - [Conda (Starting and managing)](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html#getting-started-with-conda) 
     
     By typing `conda --version` in a terminal command line verify that 
     conda is installed properly on your system (Conda displays the number of the version that you have installed). 
     
     By typing `conda update conda` and then `y` (if needed) in a terminal command line, update conda to the current version.

     1. **Anaconda Prompt:** From the Start menu, search for and open "Anaconda Prompt". 
     2. **Windows`conda create --name envname` Command Prompt:** From the Start menu, search for and open "cmd". 
        - When I typed `conda --version` in the Command Prompt, I encountered `conda is not recognized as an internal or external command,
          operable program or batch file`. This issue was resolved by **Method 3** of this [page](https://appuals.com/fix-conda-is-not-recognized-as-an-internal-or-external-command-operable-program-or-batch-file/).
   - [Managing environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#managing-environments)
       - Some useful command lines:
            1) `conda create --name envname` or `conda create -n envname`, to create an environment with the name "envname".
                - Create seperate environments to keep your programs isolated from each other.
            2) `conda activate envname`, to activate the environment "envname".
            3) `conda info --envs`, to see a list of all your environments (The active environment is with an asterisk (*)).
            4) `conda deactivate`, to deactivate environment.
                - `conda activate` and `conda deactivate` only work on conda 4.6 and later versions. 
            5) `conda list -n envname` or `conda list`, to see a list of all packages installed in a specific environment "envname". 
            6) `conda list -n envname pkgname`, to see if a specific package "pkgname" is installed in an environment "envname".
            7) `conda install --revision=0` or `conda install --rev 0`, to restore environment to the default version.
            
### :star: Other useful links

   - GitHub: [Applied Machine Learning](https://github.com/hhaji/Applied-Machine-Learning) by Hossein Hajiabolhassan
   - GitHub: [Tools in Data Science](https://github.com/hhaji/Tools-in-Data-Science) by Hossein Hajiabolhassan
