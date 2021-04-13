# Hakuna my data
R codes and data accompanying the paper "Understanding the reliability of citizen science observational data using item response models" to appear in Methods in Ecology and Evolution.

__Authors:__

*Edgar Santos-Fernandez*, PhD. School of Mathematical Sciences. Y Block, Floor 8, Gardens Point Campus
Queensland University of Technology. GPO Box 2434. Brisbane, QLD 4001. Australia

*Kerrie Mengersen*, Dist. Professor of Statistics. Deputy Director, ARC Centre for Mathematical and Statistical Frontiers;
Director, QUT Centre for Data Science. School of Mathematical Sciences. Y Block, Floor 8, Gardens Point Campus.
Queensland University of Technology. GPO Box 2434. Brisbane, QLD 4001. Australia


The paper can be found at:

* https://arxiv.org/abs/2003.06966
* https://www.researchgate.net/publication/339944525_Bayesian_item_response_models_for_citizen_science_ecological_data

The models introduced in the article are part of the R package **staircase** (https://github.com/EdgarSantos-Fernandez/staircase).


## Results from the item response models:

![Alt text](https://github.com/EdgarSantos-Fernandez/hakuna/blob/main/seren_abil.jpg?raw=true "Title")
Fig: Estimates of the users' abilities vs their proportion of correct classification.

![Alt text](https://github.com/EdgarSantos-Fernandez/hakuna/blob/main/prob_vs_species.jpg?raw=true "Title")
Fig: Species difficulties vs the proportion of correct classification.

## Files in this repository:

1- _Codes_used_in_Item_response_modeling_for_big_data.Rmd_ illustrate the implementation of the case study from  Section 4.3 (Item response model for big data).
The first part contains the codes for fitting the model using Stan on a High-Performance Computing system (HPC).
We then show how to combine the subposterior estimates via consensus Monte Carlo.


2- serengeti.RDS is the dataset used in the case study. 
It includes the following variables:
-	LocationX and LocationY: X and Y coordinates of the site.
- DateTime: classification time stamp.
-	UserID: unique user identifier.
-	SiteID: site identification code.
- Species: classification value. 
-	True_Species: true species obtained from the gold standard dataset or via consensus voting.
-	Correct: outcome of the classification (1 = correct, 0 = otherwise).
- set: Data was split into 10 shards using stratified sampling. 

See Swanson et al. (2015) for more details.

## How to cite:
Santos-Fernandez, Edgar, and Mengersen, Kerrie . "Bayesian item response models for citizen science ecological data." arXiv preprint arXiv:2003.06966 (2020).


## References:

Swanson, A., M. Kosmala, C. Lintott, R. Simpson, A. Smith, and C. Packer (2015).
Snapshot Serengeti, high-frequency annotated camera trap images of 40 mammalian species in an African savanna. Scientific data 2, 150026.
=======


