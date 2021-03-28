# NN_MM-GBSA

Assuming we are in the root_dir of NN_MM-GBSA folder.

To prepare the training/test set with MD/MM-GBSA raw data:
```
cd Data
./torch_prep_kfold.py 0.0 0 240 ../Mater/rawdat_1.csv ../Mater/rawdat_2.csv ../Mater/rawdat_3.csv ../Mater/rawdat_4.csv
cd ..
```

To perform training and testing with MD/MM-GBSA results using 5-fold cross-validation:
```
./nn_kfold.py 1
```

To train a model with all data and make predictions on unknown variants, comment line #353 and uncomment line #355
```
./nn_kfold.py 1
./nn_kfold.py 2
```