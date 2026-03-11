# Modeling the distribution of _Triquetrella californica_

## Jake Bauer - California State University, Los Angeles

_Triquetrella californica_ is a rare moss endemic to the Pacific coast of North America from San Diego, CA up to the Gulf Islands, BC. Despite it's large range, only a handful of populations are known for this species. Given anthropogenic threats to it's coastal habitat, predicting the distribution of _T. californica_ is an important conservation task.

<img src="https://inaturalist-open-data.s3.amazonaws.com/photos/350795815/large.jpg" alt="Triquetrella californica" style="width:500px;height:300px;">

The primary goal of this project is to apply modeling and field work to produce and validate species distributions for _T. californica_ iteratively. The iterative methods used are to be loosely inspired by the techniques used for modeling _Ivesia webberi_ (<a href="https://www.int-res.com/articles/esr2023/50/n050p047.pdf" target="_blank">Borokini, 2023</a>). At least until the distribution is better known with more field data, this model aims for predictive power over causal inference. A Bayesian framework will be used to get the most out of a small amount of occurence data. The Bayesian modeling process is largely inspired by McElreath's <a href="https://github.com/rmcelreath/stat_rethinking_2026" target="_blank">_Statistical Rethinking_</a> resources.

This GitHub repository is an attempt to keep my process as reproducible as possible. For any questions, please reach out to jbauer3@calstatela.edu

# DATA

The study area for this project includes California, Oregon and Washington. Datapoints of _T. californica_ are available for British Columbia, however contiguous datasets that include San Diego through British Columbia are uncommon. For the iterative modelling, current field work will be restriced to Southern California for transportation reasons, and initially will be restricted to Mission Trails Regional Park, where permits are already aquired through the San Diego State University Herbarium. When applicable, 2020 datasets were chosen.

Datasets considered include the 6 uncorrelated variables determined by Borokini,
<ul>
  <li>*Cosine aspect</li>
  <li>*Topographic Position Index (TPI333)</li>
  <li>*Perennial herbaceous cover</li>
  <li>Cumulative annual actual evapo-transpiration</li>
  <li>Minimum monthly temperature</li>
  <li>Summer seasonal precipitation</li>
</ul>
as well as additional datasets that were considered possible indicators for _T. californica_ based on field experience:
<ul>
  <li>*Elevation</li>
  <li>*Land cover</li>
  <li>*Topographic Wetness Index</li>
  <li>*Topographic Position Index (TPI33)</li>
  <li>*Annual herbaceous cover</li>
  <li>*Bare ground</li>
  <li>*Soil litter</li>
  <li>*Shrub cover</li>
  <li>*Tree cover</li>
  <li>Solar radiation</li>
  <li>Available water content</li>
  <li>Geology: lithology</li>
  <li>Geology: presence of granitic incidentals</li>
  <li>Fog</li>
  <li>Distance to water bodies</li>
  <li>Distance to hydrological network</li>
  <li>Bird abundance</li>
  <li>Bird stopover</li>
  <li>Cloud cover</li>
  <li>Geomorphons</li>
</ul>


# Downloading Files
Because rasters used in this project are large, and originate from many source agencies, instructions for the downloading these products are included below:

## TNM DEM (1 arc second)
Data query was generated for the study area using <a href="https://apps.nationalmap.gov/downloader/" target="_blank">TNM Download v2.0</a>.  To download the queried files, <a href="https://sourceforge.net/projects/urlget/" target="_blank">uGet</a> was utilized. Use <a href="https://github.com/jakejbauer/triquetrella-model/blob/main/NED_1arcsec_StudyArea_uGet.txt" target="_blank">NED_1arcsec_StudyArea_uGet.txt</a> to initiate a uGet download.

## Multi-Resolution Land Characteristics
Data for all MRLC (both RCMAP and NRLC) datasets can be downloaded directly from their <a href="https://www.mrlc.gov/data" target="_blank">MRLC Consortium page</a>. Datasets used include the following:
<ul>
  <li>Land Cover</li>
  <li>Annual Herbaceous Cover</li>
  <li>Bare ground</li>
  <li>Perennial Herbaceous Cover</li>
  <li>Soil Litter</li>
  <li>Shrub Cover</li>
  <li>Shrub Height</li>
  <li>Tree Cover</li>
</ul>

## USGS Geologic map
Geodatabase with geologic data (Horton et al. 2017) downloaded from the <a href="https://mrdata.usgs.gov/geology/state/" target="_blank">USGS Geologic maps of the US states webpage.</a>

