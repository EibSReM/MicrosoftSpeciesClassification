# MicrosoftSpeciesClassification

Script to classify images of plants and animals with the image-based species recognition models provided by Microsoft AI for Earth. The code was extracted from this Microsoft [repository](https://github.com/microsoft/SpeciesClassification), which can also be used for the inference on its own by following the described steps there, but it contains some more scripts which were not necessary for us and thus removed in this repository. The model is not updated anymore.

## How-To

1. Install conda / miniconda if you do not have already (see [here for installation](https://docs.conda.io/en/latest/miniconda.html) of miniconda and [here](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf) for a conda cheatsheet).

2. Create a conda environment from the `environment.yml` file by executing
```
conda env create -f environment.yml
```

3. Clone this repository by
```
git clone https://github.com/EibSReM/MicrosoftSpeciesClassification.git
``` 
and change to respective directory (`cd MicrosoftSpeciesClassification`)

4. If you want to download the pretrained pytorch model manually you can do so [here](https://github.com/microsoft/SpeciesClassification) (409 MB). This is not mandatory since the script also offers the opportunity to download the model automatically.

5. The same for the taxononmy file that you can download manually [here](https://github.com/microsoft/SpeciesClassification)

6. Adapt api_root in the `classify_images.py` script. It should be the path to the cloned repository.

7. Adapt the paths to the pytorch model, the taxonomy file and the images (folder) in the `classify_images.py` script (if you don't want to download the model and taxonomy files beforehand the script can do it for you, if you change the paths to the given hyperlinks)

8. Run script 
```
python classify_images.py
```

9. Find results in `classification_output.csv`

## Runtime
Classifying 204 images, the script run 2175 seconds (~ 36 minutes) on a Windows 10 notebook with the following hardware specifications:
* Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz   1.99 GHz
* 20 GB Ram

## Approach Demo 
In the folder [demo](/demo/) you can find a couple of images and a README with the expected results for demonstration purposes. 