
---
| :four_leaf_clover:   My Path to Machine Learning :four_leaf_clover:                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| :bulb: *Do not follow where the path may lead. Go instead where there is no path and  leave  a trail. `Ralph Waldo Emerson`*                                                                                                                                                          |

---
| [What Is Machine Learning?](https://www.oreilly.com/library/view/hands-on-machine-learning/9781491962282/ch01.html)                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| :green_book: Machine Learning is the science (and art) of programming computers so they can learn from data.                                                                                                                                                          |
| :blue_book: A slightly more general definition: Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed (Arthur Samuel-1959)                                                              |
| :orange_book: A more engineering-oriented one:  A computer program is said to learn from experience E  with respect to some task T  and some performance measure  P, if its performance on  T, as measured by  P, improves with experience  E (Tom Mitchell-1997) |

### :star:  Anaconda
  - [Installation](https://docs.anaconda.com/anaconda/install/)
    - [Installing on Windows](https://docs.anaconda.com/anaconda/install/windows/)
      - I had an issue with Anaconda installation on Windows 7, `Failed to create Anaconda menus`. With the help of an [answer](https://stackoverflow.com/a/57635204/12777699) from <a href="https://stackoverflow.com/questions/tagged/python"><img  src=https://upload.wikimedia.org/wikipedia/commons/f/f7/Stack_Overflow_logo.png width="90"/>
</a>, version 2019.03 of Anaconda (from [download archive](https://repo.continuum.io/archive/)) successfully installed.
      - After installing Anaconda on Windows 7, I encountered other problems such as crashing Windows. That's why I finally decided to install Windows 10.

  - [Conda (Starting and managing)](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html#getting-started-with-conda) 
   
    :one: `conda --version` (in a terminal command line) :arrow_right: Conda version number (if it is installed properly).
    
    :two: `conda update conda` and then `y` (if needed) :arrow_right: Update conda to the current version.

    - **Anaconda Prompt:** :one: Start menu :two: search for and open "Anaconda Prompt". 
    - **Windows Command Prompt:** :one: Start menu :two: search for and open "cmd". 
        - When I typed `conda --version` in the Command Prompt, I encountered `conda is not recognized as an internal or external command,
          operable program or batch file`. This issue was resolved by **Method 3** of this [page](https://appuals.com/fix-conda-is-not-recognized-as-an-internal-or-external-command-operable-program-or-batch-file/).
  - [Managing environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#managing-environments)
     - Some useful terminal commands:
     
       :one:`conda create --name envname` or `conda create -n envname` :arrow_right: Create the environment "envname".
              
     
       :two: `conda activate envname`:arrow_right: Activate the environment "envname".
     
       :three: `conda info --envs`:arrow_right: A list of all your environments (active environment with an asterisk (*)).
     
       :four: `conda install pkgname` :arrow_right: Install the package "pkgname" in the active environment.
         
       :five: `conda list -n envname` or `conda list`:arrow_right: A list of all packages installed in the active environment. 
     
       :six: `conda list -n envname pkgname`:arrow_right: To see if the package "pkgname" is installed in "envname".
     
       :seven: `conda install --revision=0` or `conda install --rev 0`:arrow_right: Restore active environment to the default version.
    
       :eight: `conda deactivate` :arrow_right: Deactivate environment.

       :nine: `conda remove --name envname --all`:arrow_right: Remove the environment "envname".
     - [Conda cheat sheet](https://docs.conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf)
  - Python and Jupyter Lab
     
     - Python Installation (by a terminal command line): Type `conda install python=vnumber` to install version "vnumber" of Python in the active environment.

     - Jupyter Lab Installation (by a terminal command line): Type `conda install jupyterlab` to install Jupyter Lab in the active environment.
     
     - Use `jupyter lab` to start Jupyter Lab.

     - [Installing the IPython kernel](https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments)
	    - Terminal command: `python -m ipykernel install --user --name envname --display-name "Python (envname)"`
		
  - [conda-forge](https://conda-forge.org/docs/user/introduction.html)
  
     - Installing packages from conda-forge:
		
	    - `conda config --add channels conda-forge` :arrow_right: Register the conda-forge channel as a package source for conda
			
	    - `conda config --set channel_priority strict` :arrow_right: Activate the strict channel priority.
  
### :star:  Python
   - GitHub Repository: [**Practical Python**](https://github.com/dabeaz-course/practical-python)
   - [**Python Cheat Sheet**](https://raw.githubusercontent.com/coodict/python3-in-one-pic/master/py3%20in%20one%20pic.png)

   - **Installation of python libraries:**
   	 - **Installing libraries with the command `conda install "libname"`:**
	 
	 	Some libraries could not be installed with the above command line. Then, you can either do `pip install 
		"libname"` or download the source and install that manually as follows.
	 
  	 - **Installing libraries manually:**
   
   		Download the source file of the library containing the file `setup.py` :arrow_right: Launch the anaconda prompt and 
		navigate to the folder that contains the extracted downloaded files , e.g., with the command `cd /d d:\anaconda3\tflearn-
		master`  :arrow_right: Run `python setup.py install`

### :star:  Colab
   - [**What is Colaboratory?**](https://colab.research.google.com/notebooks/intro.ipynb#scrollTo=5fCEDCU_qrC0)

   - **A good approach to import local datasets into the Colab:**
   
   		:one: Compress the dataset's folder, e.i., as a `zip` file :two: Upload the compressed file to your Google drive :three: Mount your Google drive into the 			colab :four: Unzip the compressed file in Colab.
	
   - [**To prevent Google Colab from disconnecting**](https://kapeli.com/cheat_sheets/LaTeX_Math_Symbols.docset/Contents/Resources/Documents/index): 
   
    	> Google Colab notebooks have an idle timeout of 90 minutes and absolute timeout of 12 hours. This means, if user does not interact with his Google Colab notebook for more than 90 minutes,
                   its instance is automatically terminated. Also, maximum lifetime of a Colab instance is 12 hours.
		
   		To prevent Google Colab from disconnecting, Open developer settings in your web browser with `Ctrl+Shift+I` :arrow_right: Click on console tab  :arrow_right:  Type the following code block in the console prompt:
  	 ```javascript 
   	    function ClickConnect(){
		console.log("Working"); 
		document.querySelector("colab-toolbar-button").click() 
		}setInterval(ClickConnect,60000)
  	 ```
   
### :star:  Markdown
   - [Mastering Markdown](https://guides.github.com/features/mastering-markdown/#examples) 
   - [LaTeX Math Symbols Cheat Sheet](https://kapeli.com/cheat_sheets/LaTeX_Math_Symbols.docset/Contents/Resources/Documents/index)
  
### :star:  Git
   - [Installation](https://git-scm.com/downloads)
   - [Documentation](https://git-scm.com/doc)
   - [Git Handbook (10 minute read)](https://guides.github.com/introduction/git-handbook/)
   - [Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
   - Videos (Persian): [Git](https://parsclick.net/course/PL3Y-E4YSE4wYFlcomsBtJy1nCu3jclA8L) by Amir Hasan Azimi
   - Videos (English): GitHub Ultimate-Master Git and GitHub by Jason Taylor
   
### :star:  Books
   - [Understanding Machine Learning: From Theory to Algorithms](https://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/understanding-machine-learning-theory-algorithms.pdf) by Shai Shalev-Shwartz and Shai Ben-David
   - [Hands‑On Machine Learning with Scikit‑Learn, Keras, and TensorFlow 2](https://github.com/ageron/handson-ml2) by Aurélien Geron

### :star: Other good resources

- Free online ebook: [Forecasting: principles and practice](https://otexts.com/fpp2/) by Rob J Hyndman, and George Athanasopoulos
- Brief visual explanations of machine learning concepts with diagrams: [Machine Learning Glossary](https://ml-cheatsheet.readthedocs.io/en/latest/index.html)
- Made With ML: [A collection of the best ML tutorials, toolkits and research organized by topic](https://madewithml.com/topics/)

### :star:  Other useful links

   - GitHub Repository: [Tools in Data Science](https://github.com/hhaji/Tools-in-Data-Science) by Hossein Hajiabolhassan
   - GitHub Repository: [Applied Machine Learning](https://github.com/hhaji/Applied-Machine-Learning) by Hossein Hajiabolhassan

   
### :star:  Some interesting articles

   - [20 Best Machine Learning Books for Beginner & Experts in 2020](https://hackr.io/blog/best-machine-learning-books)
   - [Difference Between Algorithm and Model in Machine Learning](https://machinelearningmastery.com/difference-between-algorithm-and-model-in-machine-learning/#:~:text=A%20model%20represents%20what%20was,structures%20required%20to%20make%20predictions.)
   - [Famous Machine Learning Datasets You Need to Know](https://medium.com/data-science-bootcamp/famous-machine-learning-datasets-you-need-to-know-dd031bf74dd) by Uniqtech
   - [10 Standard Datasets for Practicing Applied Machine Learning](https://machinelearningmastery.com/standard-machine-learning-datasets/) by Jason Brownlee
   - [5 Data Science Projects That Will Get You Hired in 2020](https://www.dataoptimal.com/data-science-projects-2018/)
   - [5 free resources every data scientist should start using today](https://thenextweb.com/growth-quarters/2020/08/08/5-free-resources-every-data-scientist-should-start-using-today-syndication/amp/) by Yitaek Hwang
   - [Seaborn Heatmaps: 13 Ways to Customize Correlation Matrix Visualizations](https://heartbeat.fritz.ai/seaborn-heatmaps-13-ways-to-customize-correlation-matrix-visualizations-f1c49c816f07) by Okoh Anita

 ### :star:  Good resources for finding datasets

   - [UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/index.php)
   - [Kaggle](https://www.kaggle.com/datasets)
   - [Elite data science](https://elitedatascience.com/datasets)
   - [Dataset search](https://datasetsearch.research.google.com/)
   
   
