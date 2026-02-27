# Modelling the distribution of _Triquetrella californica_

## Jake Bauer - California State University, Los Angeles

_Triquetrella californica_ is a rare moss endemic to the Pacific coast of North America from San Diego, CA up to the Gulf Islands, BC. Despite it's large range, only a handful of populations are known for this species. Given anthropogenic threats to it's coastal habitat, predicting the distribution of _T. californica_ is an important conservation task.

<img src="https://inaturalist-open-data.s3.amazonaws.com/photos/350795815/large.jpg" alt="Triquetrella californica" style="width:500px;height:300px;">

The primary goal of this project is to apply modelling and field work to produce and validate species distributions for _T. californica_ iteratively. The iterative methods used are to be loosely inspired by the techniques used for modelling _Ivesia webberi_ (<a href="https://www.int-res.com/articles/esr2023/50/n050p047.pdf" target="_blank">Borokini, 2023</a>). At least until the distribution is better known with more field data, this model aims for predictive power over causal inference. A Bayesian framework will be used to get the most out of a small amount of occurence data. The Bayesian modelling process is largely inspired by McElreath's <a href="https://github.com/rmcelreath/stat_rethinking_2026">_Statistical Rethinking_</a> resources.

This GitHub repository is an attempt to keep my process as reproducible as possible. For any questions, please reach out to jbauer3@calstatela.edu


# Downloading Files
Because rasters used in this project are large, and originate from many source agencies, instructions for the downloading these products are included below:

## TNIM DEM (1 arc second)
Data query was generated for the study area using <a href="https://apps.nationalmap.gov/downloader/">TNM Download v2.0</a>.  To download the queried files, <a href="https://sourceforge.net/projects/urlget/">uGet</a> was utilized. Use <a href="https://github.com/jakejbauer/triquetrella-model/blob/main/NED_1arcsec_StudyArea_uGet.txt">NED_1arcsec_StudyArea_uGet.txt</a> to initiate a uGet download.


