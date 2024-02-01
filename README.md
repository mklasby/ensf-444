# ENSF 444 LO3 Lab Materials

### Installation:
1. Fork this repo!
2. Install conda: https://conda.io/projects/conda/en/latest/user-guide/install/index.html
3. If you already have `conda` installed, make sure your `base` env is up-to-date by running: `conda update -n base conda`
4. Create `conda` environment: `conda env create --file ./environment.yaml`
5. Register for Kaggle is you do not already have an account: https://www.kaggle.com/ 
6. If you want to use kaggle API, download your kaggle.json by following instructions here: https://www.kaggle.com/docs/api?utm_me= and sign up to the competition on Kaggle website to accept competition rules. 

### Repo tour:
* Labs will be placed in subdirectories name as `lab-#` where `#` is the lab number. There will be 9 labs in total.
* Solutions to labs will be placed in `./solutions` as well as on D2L. 
* Participation marks are awarded for labs. Attend the lab as scheduled and write your name and UCID on google document that will be provided. 
* `./data` is used to store datasets we will be using for the labs. Note that files contained in this directory will not be synced with remote repo. 

### Integration with Google Collab:
* Feel free to use google collab instead of local development. You can load the notebook directly into collab and load the datasets through the GUI or with API calls, but you'll need to authenticate Kaggle on the collab instance if you want to use API. 

### Merging issues with notebooks:
Jupyter notebooks are stored as json formatted files. Each cell contains metadata such as `execution_count`, `outputs`, etc. Git doesn't know what is "important" to track, so re-running the notebook even without changing the source code can result in nasty merge conflicts. 

The best work-around for this is to use `jupytext` to convert `.ipynb` files to `.py` modules. Then we can push the `.py` files to the remote repository and convert back to notebook format on our local systems. This way only the source code is actually tracked by git. 

However, since we do not want to introduce any additional complexity to using this repo, we can use the following strategy to avoid merge conflicts:
1. Fork the repo
2. Add the upstream remote repo with the command: `git remote add upstream git@github.com:mklasby/ensf-444.git`. 
3. Whenever you want to work on a jupyter notebook that originates from the upstream repo (`mklasby/ensf-444`), **copy that notebook and rename it**. For instance, add your initials as a suffix to the file name. 
4. Now, you can pull in new updates from the repo by using the CLI command `git fetch --upstream`
5. Make sure you checkout the `main` branch if you're using different branches. This can be done with the command `git checkout main`.
6. Now we are finally ready to move our local commits to the tip of the upstream remote. This is known as "rebasing". Use the command `git rebase upstream/master`. 
7. Finally, we push this new git history (our local commits move on top of remote updates) using the command `git push -f`. Note that the "force" option `-f` is required as your local history will differ from the history on the remote origin (your github fork).