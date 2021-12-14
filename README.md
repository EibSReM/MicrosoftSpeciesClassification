# MicrosoftSpeciesClassification

Script to classify images of plants and animals with the image-based species recognition models provided by Microsoft AI for Earth. The code was extracted from this Microsoft [repository](https://github.com/microsoft/SpeciesClassification), which can also be used for the inference on its own by following the described steps there, but it contains some more scripts which were not necessary for us and thus removed in this repository. The model is not updated anymore.

## How-To

1. (recommended but not absolutely necessary) create and activate own (conda) environment 
2. install packages 
```
conda install pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=10.0 -c pytorch
pip install pretrainedmodels==0.7.4
pip install pillow==6.1.0
pip install progressbar2==3.51.0
pip install cupy-cuda100==7.3.0
pip install torchnet==0.0.4
pip install matplotlib pandas scikit-image
```
3. Clone this repository 
```
git clone https://github.com/EibSReM/MicrosoftSpeciesClassification.git
``` 
and change to respective directory
4. Download pretrained pytorch model mentioned [here](https://github.com/microsoft/SpeciesClassification). This is not mandatory since the script also offers the opportunity to download the model if you change the path to the respective hyperlink (included in the script but commented out).
5. Download taxonomy file mentioned [here](https://github.com/microsoft/SpeciesClassification)
6. Adapt path to pytorch model, taxonomy file and images (folder) in the `classify_images.py` script (if you don't want to download the model and taxonomy files beforehand the script can do it for you, if you change the paths to the given hyperlinks)
7. Run script 
```
python classify_images.py
```
8. Find results in `classification_output.csv`

