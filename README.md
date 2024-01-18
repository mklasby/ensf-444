# ENSF 444 LO3 Lab Materials

### Installation:
1. Fork this repo!
2. Install conda: https://conda.io/projects/conda/en/latest/user-guide/install/index.html
3. If you already have `conda` installed, make sure your `base` env is up-to-date by running: `conda update -n base conda`
4. Create `conda` environment: `conda env create --file ./environment.yaml`
5. Register for Kaggle is you do not already have an account: https://www.kaggle.com/ 
6. If you want to use kaggle API, download your kaggle.json by following instructions here: https://www.kaggle.com/docs/api?utm_me= and sign up to the competition on Kaggle website to accept competition rules. 

### Repo tour
* Labs will be placed in subdirectories name as `lab-#` where `#` is the lab number. There will be 9 labs in total.
* Solutions to labs will be placed in `./solutions` as well as on D2L. 
* Participation marks are awarded for labs. You have two options to receive the mark for each lab: 
    1. Attend the lab as scheduled and write your name and UCID on google document that will be provided
    2. Complete lab notebook *before* the scheduled lab and submit via email to me: mklasby AT ucalgary DOT ca
* `./data` is used to store datasets we will be using for the labs. Note that files contained in this directory will not be synced with remote repo. 

### Integration with Google Collab
* Feel free to use google collab instead of local development. You can load the notebook directly into collab and load the datasets through the GUI or with API calls, but you'll need to authenticate Kaggle on the collab instance if you want to use API. 