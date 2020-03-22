# <center>All cmd items are here</center>
I tend to forget important commands all the time therefore, I have created this doccument to list all frequently used cmds here (technology wise).

## <center> Git </center>
cmds for git setup: 

- `git init`  

	> Initialize a local git repo  

- `git config --global user.name` : dinabandhu50  

	> Add username to global git

- `git config --global user.email`: beheradinabandhu50@gmail.com  

	> Add user email to global git

- `git remote add origin https://github.com/dinabandhu50/ABALONE_PROJECT.git`  

	> This will connect the github repository to remote with name origin.

- `git clone https://github.com/dinabandhu50/ABALONE_PROJECT.git`  

	> Clone a git repository to local.

- `git pull https://github.com/dinabandhu50/ABALONE_PROJECT.git`  

	> This will pull the repository from github but you will have to set the origin using `git remote add origin https://github.com/dinabandhu50/ABALONE_PROJECT.git`  

cmds for pushing code:

- `git add .` or `git add *.html`  

	> This command adds changed files to git buffer

- `git commit -m "First commit"`  

	> commit something to github buffer

- `git push -u origin master`  

	> push updated codes  

cmds for large files :  
- `git lfs track "*.csv"`  

	> add the big data file in lfs tracker

- `git add .`  
- `git commit -m "added large file"`  
- `git push -u origin master`  

## <center> conda </center>

basic conda:

- `conda activate myenv`   

	> activate conda virtual environment  
- `conda list`  

	> list all installe packages  

- `conda install [package]`  

	> install any conda package

- `pip install [package]`  

	> pip install package inside conda env  

- `conda remove --name [myenv] --all`  

	> remove conda environment

virtual environment manage:

- `pip freeze > requirement.txt`  
	
	> This will write down all packages along with their version installed in that conda environment  

- `conda env export > conda.yml` 

	> This will build a conda environment file specific to OS. you cannot use this `conda.yml` in Ubuntu if it is generated from Windows.  

- `conda env export --no-builds > conda.yml`  
	
	> This file can be used in both Ubuntu and Windows as OS specific build infrmation is written into `conda.yml`, but it will contain all the dependencies packages specific to OS (Windows/ Ubuntu etc.) hence it may fail to reproduce the same environment in different OS.  
- `conda env export --from-history > conda.yml`

	> This file will contain only main packages which we have installed using `conda install [packages]`. the `pip install [packages]` won't be there.  

reproducing conda environment using my steps:
- `conda env export --no-buids > conda.yml`  
	> This is for scenario, when the project and virtual environment is created in an OS (Ubuntu/Windows) and again need to reproduce the same virtual environment in same corresponding OS (Ubuntu/Windows).

- Manually writedown all packages you are installing in that env  

	> such as 
	> - `conda install pip`
	> - `conda install nb_conda`
	> - `pip install numpy matplotlib pandas scikit-learn`
	> - `pip install tensorflow`
	> - `pip install pytorch`

- Edit the `conda.yml` file created using `--no-builds`  

	> Manually keep only those packages which you recognize installing, remove all dependencies. This way one can use the `conda.yml` file in both Windows and Ubuntu system.

- Basically create 3 to 4 files in `env` folder  

	> `env/env_windows.yml`  or  `env/env_ubuntu.yml`  
	> `env/manual_conda.yml`  
	> `env/hand_entry_env.yml`  


## <center> vscode </center>

vscode settings (windows):

```json
{
    // "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
    "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\cmd.exe",
    "python.linting.pylintArgs": [
        "--extension-pkg-whitelist=cv2"
    ],
    "workbench.colorTheme": "Dracula At Night",
    // "editor.quickSuggestionsDelay": 1000,
    // "editor.hover.enabled": false,
    // "editor.parameterHints": false,
    "editor.parameterHints": false,
    "explorer.confirmDragAndDrop": false,
    "editor.fontSize": 16,
    // "editor.parameterHints.enabled": false
    // "editor."
    "editor.formatOnSave": true,
    "python.formatting.provider": "autopep8",
    "workbench.iconTheme": "material-icon-theme",
    "python.dataScience.sendSelectionToInteractiveWindow": true,
    "terminal.integrated.inheritEnv": false
}
```

vscode extensions:

-	Auto Rename Tag
-	Beautify
-	Bracket Pair Colorizer
-	Dracula At Night
-	markdownlint
-	Material Icon Theme
-	Material Theme
-	Night Owl
-	One Dark Pro
-	Prettier - Code formatter
-	Python

## <center> Docker </center>
> To be filled  

## <center> Heroku </center>
> To be filled
