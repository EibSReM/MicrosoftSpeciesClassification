# Approach Demo 
In the folder [images](/demo/images/) you can find a couple of images. For these images, we show here exemplary how we calculated the accuracy for the different computer vision models. 

Typically, for a given image, the models return species as a prediction, including the probability that the species depicted on the image actually matches the prediction. Thereby, it differs by model how many predictions are returned. To determine the accuracy of the models, we decided to calculate the Top-1 and Top-5 accuracy. If the first prediction of a model is correct, it is a Top-1 prediction and if one of the first five predictions of a model is correct, it is within the Top-5 predictions. The calculation of the Top-5 accuracies can be interesting to decide if the model is helpful to show citizens 5 predictions from which they can indicate the observed one. Thus, the percentage given by the Top-1 or Top-5 accuracy indicates for how many of the images contained in the test dataset the prediction was correct or within the Top-5, respectively. 

The rank indicates which of the first five predictions by the model was correct. 
If 'n/a' is entered as a value in the tables below, no prediction was returned by the model or, with respect to the rank, no correct prediction among the first 5 predictions was returned by the respective model. 

## iNat2021 
Image                                                                       | Prediction    | Propability  | Rank
:-----                                                                      | :----:        | -----:            | -----:
<img src="images/myocastor_coypus.jpg" alt="drawing" width="50"/>           | **Myocastor coypus** <br> Ondatra zibethicus <br> Castor canadensis <br> Lontra canadensis <br> Microtus pennsylvanicus           | 0.81 <br> 0.08 <br> 0.06 <br> 0.01 <br> 0.01 | 1
<img src="images/asclepias_syriaca.jpg" alt="drawing" width="50"/>          | Asclepias speciosa <br> **Asclepias syriaca** <br> Asclepias eriocarpa <br> Wyethia mollis <br> Calotropis procera     | 0.50 <br> 0.41 <br> 0.03 <br> 0.01 <br> 0.01 | 2
<img src="images/lithobates_catesbeianus.jpg" alt="drawing" width="50"/>    | Terrapene ornata <br> Caiman crocodilus <br> Apalone spinifera <br> Stigmochelys pardalis <br>  Lithobates septentrionalis       | 0.18 <br> 0.13 <br> 0.09 <br> 0.07 <br> 0.06 | n/a

The correct prediction is written in bold. The accuracies calculated with the examples in the table are: Top-1 accuracy: 33.33 % (1 out of 3 correct in the first prediction), Top-5 accuracy: 66.67 % (2 out of 3 correct in the first five predictions). The species depicted in the last example is Lithobates catesbeianus. 

## iNaturalist API
Image                                                                       | Prediction    | Propability  | Rank
:-----                                                                      | :----:        | -----:            | -----:
<img src="images/myocastor_coypus.jpg" alt="drawing" width="50"/>           | **Myocastor coypus** <br> Hydromys chrysogaster <br> Marmota flaviventris <br> Cercopithecus mitis <br> Lontra canadensis           | n/a <br> n/a <br> n/a <br> n/a <br> n/a | 1
<img src="images/asclepias_syriaca.jpg" alt="drawing" width="50"/>          | **Asclepias syriaca** <br> Asclepias speciosa <br> Asclepias sullivantii <br> Cunonia capensis <br> Asclepias glaucescens       | n/a <br> n/a <br> n/a <br> n/a <br> n/a | 1
<img src="images/lithobates_catesbeianus.jpg" alt="drawing" width="50"/>    | Lithobates montezumae <br> Pelophylax bedriagae <br> Pelophylax ridibundus <br>  Pelophylax perezi <br>  Rana draytonii        | n/a <br> n/a <br> n/a <br> n/a <br> n/a | n/a

The correct prediction is written in bold. The accuracies calculated with the examples in the table are: Top-1 accuracy: 66.67 % (2 out of 3 correct in the first prediction), Top-5 accuracy: 66.67 % (2 out of 3 correct in the first five predictions). The species depicted in the last example is Lithobates catesbeianus. For the predictions by iNaturalist no propability was delivered. 

## Microsoft Species Classification
Image                                                                       | Prediction    | Propability  | Rank
:-----                                                                      | :----:        | -----:            | -----:
<img src="images/myocastor_coypus.jpg" alt="drawing" width="50"/>           | **Myocastor coypus** <br> Castor canadensis <br> Ondatra zibethicus <br> Hydrochoerus hydrochaeris <br> Lontra canadensis           | 0.873 <br> 0.04 <br> 0.007 <br> 0.005 <br> 0.003 | 1
<img src="images/asclepias_syriaca.jpg" alt="drawing" width="50"/>          | **Asclepias syriaca** <br> Asclepias speciosa <br> Asclepias eriocarpa <br> Asclepias viridiflora <br> Asclepias linaria       | 0.582 <br> 0.305 <br> 0.026 <br> 0.008 <br> 0.006 | 1
<img src="images/lithobates_catesbeianus.jpg" alt="drawing" width="50"/>    | **Lithobates catesbeianus** <br> Lithobates berlandieri <br> Lithobates clamitans <br>  Rana temporaria <br>  Rana draytonii       | 0.835 <br> 0.025 <br> 0.024 <br> 0.015 <br> 0.015 | 1

The correct prediction is written in bold. The accuracies calculated with the examples in the table are: Top-1 accuracy: 100 % (3 out of 3 correct in the first prediction), Top-5 accuracy: 100 % (3 out of 3 correct in the first five predictions).

## Nature Identification API (NIA) 
Image                                                                       | Prediction    | Propability  | Rank
:-----                                                                      | :----:        | -----:            | -----:
<img src="images/myocastor_coypus.jpg" alt="drawing" width="50"/>           | **Myocastor coypus** <br> Ondatra zibethicus <br> Sus scrofa <br> Castor fiber <br> Phoca vitulina           | 0.9998825788 <br> 6,88E+10 <br> 2,10E+10 <br> 1,48E+11 <br> 3,90E+09 | 1
<img src="images/asclepias_syriaca.jpg" alt="drawing" width="50"/>          | **Asclepias syriaca** <br> Hyla arborea <br> Cydalima perspectalis <br> Caloptilia stigmatella <br> Smerinthus ocellatus       | 0.3324504793 <br> 0.2853876054 <br> 0.03728974983 <br> 0.03603673354 <br> 0.03525354341 | 1
<img src="images/lithobates_catesbeianus.jpg" alt="drawing" width="50"/>    | Pelophylax spec. <br> Rana temporaria <br> Pelophylax lessonae <br>  Pelophylax ridibundus <br>  Pelophylax kl. esculentus       | 0.613794446 <br> 0.1141380891 <br> 0.06552799046 <br> 0.0512454994 <br> 0.03507460654 | n/a

The correct prediction is written in bold. The accuracies calculated with the examples in the table are: Top-1 accuracy: 66.67 % (2 out of 3 correct in the first prediction), Top-5 accuracy: 66.67 % (2 out of 3 correct in the first five predictions). The species depicted in the last example is Lithobates catesbeianus. 

## Pl@ntNet-API
Image                                                                       | Prediction    | Propability   | Rank
:-----                                                                      | :----:        | -----:            | -----:
<img src="images/gunnera_tinctoria.jpg" alt="drawing" width="50"/>           | **Gunnera tinctoria** <br> n/a <br> n/a <br> n/a <br> n/a          | 0.25288 <br> n/a <br> n/a <br> n/a <br> n/a | 1
<img src="images/asclepias_syriaca.jpg" alt="drawing" width="50"/>          | **Asclepias syriaca** <br> Asclepias speciosa <br> Asclepias latifolia <br> Asclepias vestita <br> Asclepias erosa       | 0.4268 <br> 0.39717 <br> 0.03072 <br> 0.0272 <br> 0.01281 | 1
<img src="images/ludwigia_grandiflora.jpg" alt="drawing" width="50"/>    | **Ludwigia grandiflora** <br> Ludwigia peploides <br> n/a <br>  n/a <br>  n/a       | 0.87854 <br> 0.11198 <br> n/a <br> n/a <br> n/a | 1

The correct prediction is written in bold. The accuracies calculated with the examples in the table are: Top-1 accuracy: 100 % (3 out of 3 correct in the first prediction), Top-5 accuracy: 100 % (3 out of 3 correct in the first five predictions). 

## Plant.id API
Image                                                                       | Prediction    | Propability  | Rank
:-----                                                                      | :----:        | -----:            | -----:
<img src="images/gunnera_tinctoria.jpg" alt="drawing" width="50"/>           | **Gunnera tinctoria** <br> Gunnera <br> Gunnera manicata <br> Rheum <br> Heracleum sphondylium           | 0.6391498247 <br> 0.1985945135 <br> 0.05868734624 <br> 0.0165985485 <br> 0.01614800067 | 1
<img src="images/asclepias_syriaca.jpg" alt="drawing" width="50"/>          | **Asclepias syriaca** <br> Asclepias speciosa <br> n/a <br> n/a <br> n/a       | 0.9480034621 <br> 0.03453290734 <br> n/a <br> n/a <br> n/a | 1
<img src="images/ludwigia_grandiflora.jpg" alt="drawing" width="50"/>    | **Ludwigia grandiflora** <br> Ludwigia peploides <br> Ludwigia octovalvis <br> n/a <br>  n/a       | 0.8573716058 <br> 0.09132727917 <br> 0.01041655874 <br> n/a <br> n/a | 1

The correct prediction is written in bold. The accuracies calculated with the examples in the table are: Top-1 accuracy: 100 % (3 out of 3 correct in the first prediction), Top-5 accuracy: 100 % (3 out of 3 correct in the first five predictions). 












