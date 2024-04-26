# AudioClassifier-GMM
Diana Maxima Držíková (xdrzik01)

The goal of this project is to create classifiers which can detect one specific person in the provided dataset. 
Two models were created - GMM for audio classification.

## Audio Classifier - GMM

For audio classification, Gaussian Mixture Model was created. The model contains two Gaussians - one for the target and non-target.
Files are using library **ikrlib.py**, which was modified to match python3.10.

Three files were created and are handled like this:

``` python3.10 trainGMM [--cv]```

where:
- cv = Stands for the bool parameter which allows cross-validation to be executed. If not called, the default is *false*.

The models after training are stored in **models/GMM/new** as **gmm_target_model.pkl** and **gmm_nontarget_model.pkl**.

``` python3.10 evaluateGMM [--input filepath] [--output filepath] [--target filepath] [--non_target filepath]```

where:
- input = Input files path that are evaluated. Default *SUR_projekt2023-2024_eval*.
- output = Output file path where predictions are stored. Default **models/GMM/new/predictions.txt**.
- target = File with parameters of Gaussian for the target. Default *models/GMM/trained/gmm_target_model.pkl*.
- non_target = File with parameters of Gaussian for non-target. Default *models/GMM/trained/gmm_nontarget_model.pkl*.

Put **SUR_projekt2023-2024_eval in root folder**.

``` libGMM.py ``` is not supposed to be called on its own.

