# View From The Top : Feature Detection of Aerial Imagery

## Data Challenge Task
###### classifying a high resolution aerial image into 9 types of urban land cover; trees, grass, soil, concrete, asphalt, buildings, cars, pools, shadows

## Data Challenge Bounty
### AWS Credits Worth USD 2500
to the **two** highest ranked model submissions, based on Git timestamps 
[credits valid till February 2019, courtesy of [Amazon Web Services](https://aws.amazon.com/?nc2=h_lg)]
### USD 100 
to the **third** highest ranked model submission, based on Git timestamps
[Prize Money Courtesy of [Africa's Talking](https://africastalking.com/)]

## Due Date: 7th September 2018

## Why is this Important?

Maps are absolutely essential for decision support. Knowing where buildings are located is a fundamental input for urban planning, public safety, public health, disaster response, environmental protection, sustainable development and census data, among other examples. Some of these applications typically require timely and high-resolution maps.

Increasingly, aerial imagery of larger areas can be covered using small commercial mapping drones. As such, aerial imagery is quickly becoming a Big Data problem. A single 20-minute drone flight can capture 800 high-resolution images, for example. Academic research has shown that trained analysts will take ~ 1 minute to analyze a single high-resolution image. Manually analyzing 800 images from a 20-minute flight can therefore take 13 hours.


###### Rules of Engagement
The Data Challenge is judged based on the following criteria:
  - A Correct fork, branch and pull request
  - Using the GitHub Pull Request timestamp where order of submissions is applicable
  - Using solution quality/accuracy and explanation to rank submissions where applicable 
  - Do not share any code that you cannot open source on the Git Repository as its open source and african.ai will not be liable for any breach of intellectual property (if at all) once shared on the platform.

## Working on the Data Challenge
1.Fork the code challenge repository provided.

2.Make a topic branch. In your github form, keep the master branch clean. When you create a branch, it essentially will be a copy of the master.

>Pull all changes, make sure your repository is up to date

```sh
$ cd challenge2_ViewFromTheTop
$ git pull origin master
```

>Create a new branch as follows-> git checkout -b [your_github_username], e.g.

```sh
$ git checkout -b Witty-Kitty master
```

>See all branches created

```sh
$ git branch
* Witty-Kitty
  master
```

>Push the new branch to github

```sh
$ git push origin -u Witty-Kitty
```

3.**Remember to only make changes to the branch!**
The folder named **data** contains 2 csv files: 
* urban_land_cover_train.csv
* urban_land_cover_test.csv

The folder named **submission** contains 1 csv file:
* urban_land_cover_sample_submission.csv

The train dataset contains labelled records, ie. their classes are known.
* use the train dataset to train a satisfactory classification model
* use the model to classify the records in the test dataset
* ensure the format of your submission file is similar to the **urban_land_cover_sample_submission.csv** file in the **submission** folder
* once satisfied with the model and the predictions, name the file containing labelled test data **urban_land_cover_predictions.csv** and include it in the **submission** folder  
* Add to the base of the existing README file a brief explanation about your solution outlining the algorithm you chose to use, why you chose it and how the algorithm compared to any others you may have tried to use  

4.Commit the changes to your branch.

5.Make a pull request to the **challenge2_ViewFromTheTop** Repo.


##### Dataset Details

The dataset provided contains training and testing data for classifying a high resolution aerial image into 9 types of urban land cover. 

The land cover classes are: 
* trees 
* grass 
* soil 
* concrete 
* asphalt 
* buildings 
* cars 
* pools 
* shadows

Multi-scale spectral, size, shape, and texture information are used for classification. 

There are a low number of training samples for each class (14-30) and a high number of classification variables (148), so it may be an interesting data set for testing **feature selection methods**. 

The testing data set is from a random sampling of the image. 

###### Legend Class: Land cover class (nominal) 
* BrdIndx: Border Index (shape variable) 
* Area: Area in m2 (size variable) 
* Round: Roundness (shape variable) 
* Bright: Brightness (spectral variable) 
* Compact: Compactness (shape variable) 
* ShpIndx: Shape Index (shape variable) 
* Mean_G: Green (spectral variable) 
* Mean_R: Red (spectral variable) 
* Mean_NIR: Near Infrared (spectral variable) 
* SD_G: Standard deviation of Green (texture variable) 
* SD_R: Standard deviation of Red (texture variable) 
* SD_NIR: Standard deviation of Near Infrared (texture variable) 
* LW: Length/Width (shape variable) 
* GLCM1: Gray-Level Co-occurrence Matrix [i forget which type of GLCM metric this one is] (texture variable) 
* Rect: Rectangularity (shape variable) 
* GLCM2: Another Gray-Level Co-occurrence Matrix attribute (texture variable) 
* Dens: Density (shape variable) 
* Assym: Assymetry (shape variable) 
* NDVI: Normalized Difference Vegetation Index (spectral variable) 
* BordLngth: Border Length (shape variable) 
* GLCM3: Another Gray-Level Co-occurrence Matrix attribute (texture variable) 

###### NB: 
* These variables repeat for each coarser scale (i.e. variable_40, variable_60, ...variable_140)
* **What is a coarse scale?** When you reduce an image, you get an image at a coarser scale, while the original is the finer scale. With a reduced version of an image, each pixel can only describe a coarse/big element of the scene. Therefore in a big/unreduced image there are fine details and in a small/reduced image, only coarser details.


 
##### Resources
You can use the following resources to to get acquainted with some feature selection techniques:
* [Sci-Kit Learn Feature Selection](http://scikit-learn.org/stable/modules/feature_selection.html)

###### Terms and Conditions
  - Each individual can participate in as many challenges as they wish
  - Forks per Data Challenge need to be an individual's unique github username eg. ```Witty-Kitty```
  - Multiple submissions are allowed for as long as the challenge is still open, once the challenge is closed, the last submitted changes will be the evaluated solution
  - african.ai reserves the right to announce the winners
  - african.ai reserves the right to reward the winners based on african.ai criterion
  - Do not share any code that you cannot open source on the Git Repository as it is public and african.ai will not be liable for any breach of intellectual property (if any) once shared on the platform.
  - Data Challenges are time bound - the time restriction is specified on each challenge
  - Additional rules MAY be provided on the code challenge and will vary for each challenge
  - You are free to use all manner of tools
  - Successive interviews for projects MAY be run to satisfy participating african.ai partners






