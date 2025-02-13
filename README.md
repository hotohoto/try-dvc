## DVC storage project

```sh
git init
pip install -r requirements.txt
dvc init
dvc remote add -d myremote /home/hotohoto/playground/dvc_storage
git add .gitignore requirements.txt README.md .dvc
dvc add models/model1.txt
dvc add models/model2.txt
dvc add 3d_models/ship1.txt
dvc add 3d_models/ship2.txt
dvc push
git commit -m "Set up DVC storage"
```

## another project with DVC initialization

```sh
git clone git@github.com:hotohoto/try-dvc.git
cd try-dvc
dvc pull models/model1.txt
dvc add models/model3.txt
dvc push
git commit -m "Add model3.txt"
```

## another project without DVC initialization

```sh
pip install dvc
dvc get git@github.com:hotohoto/try-dvc.git models/model1.txt
```
