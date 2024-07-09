# Reproduction and Reanalysis of Kang et al 2020 Spatial Accessibility of COVID-19 Health Care Resources

This study is a replication of:

> Kang, J. Y., A. Michels, F. Lyu, Shaohua Wang, N. Agbodo, V. L. Freeman, and Shaowen Wang. 2020. Rapidly measuring spatial accessibility of COVID-19 healthcare resources: a case study of Illinois, USA. *International Journal of Health Geographics* **19** (1):1–17. DOI:[10.1186/s12942-020-00229-x](https://doi.org/10.1186/s12942-020-00229-x).

## Abstract

The original paper is an implementation of the enhanced two-step floating catchment area (E2FCA) method of spatial accessibility measurement in health geography, applied to accessibility of intensive care unit beds and ventilators in the state of Illinois for vulnerable people aged 50 or over or diagnosed with COVID-19. The study is significant in its use of parallel processing and cyberinfrastructure, implemented on the [CyberGISX](https://cybergisx.cigi.illinois.edu) system, and the study provides reproducibility and transparency for the COVID-19 spatial health services accessibility dashboard, [Where COVID-19](https://wherecovid19.cigi.illinois.edu/).

## Authors

- [Joseph Holler](http://www.middlebury.edu/academics/geog/faculty/node/454160)
- [Kufre Udoh](https://kufreu.github.io)
- [Derrick Burt](https://derrickburt.github.io)
- [Peter Kedron](https://sgsup.asu.edu/peter-kedron)
- [Benjamin Cordola](https://benjamincordola.github.io/)
- [GEOG 323 Classes of Spring 2021 and Fall 2021](https://gis4dev.github.io)

## Repository Documents

- Preregistration: https://osf.io/my_study
- Publication: https://doi.org/my_study
- Pre-analysis plan: [docs/report/preanalysis.pdf](docs/report/preanalysis.pdf)
- Study report: [docs/report/report.pdf](docs/report/report.pdf)
- Manuscript: [docs/manuscript/manuscript.pdf](docs/manuscript/manuscript.pdf)

## Repository Contents

The contents of this repository are outlined in three tables:
- Data: [data/data_metadata.csv](data/data_metadata.csv)
- Procedures: [procedure/procedure_metadata.csv](procedure/procedure_metadata.csv)
- Results: [results/results_metadata.csv](results/results_metadata.csv)

The [template_readme.md](template_readme.md) file contains more information on structure and rationale of this research template repository, as well as important references and licenses.


# Original Accessibility Notebook readme.md Content

> The content below is from the root `readme.md` document for the original [Where COVID-19 Accessibility repository](https://github.com/cybergis/COVID-19AccessibilityNotebook) as of [April 21, 2021](https://github.com/cybergis/COVID-19AccessibilityNotebook/commit/3b4109fb2d513a61b40f97674b2277368e9494e6).

[![CyberGISX](results/figures/original/CyberGISXLogo.svg)](https://cybergisxhub.cigi.illinois.edu/)

### Spatial Accessibility to ICU Beds and Ventilators in Illinois

<div>
    <img src="results/figures/original/ChicagoResult.png" height="450" width="350"/>
    <img src="results/figures/original/IllinoisResult.png" height="450" width="350"/>
</div>

**Authors:** Jeon-Young Kang, Alexander Michels, Fangzheng Lyu, Shaohua Wang, Nelson Agbodo, Vincent L. Freeman & Shaowen Wang

**Paper:** https://doi.org/10.1186/s12942-020-00229-x

**Abstract:** This aims to measure spatial access for people to hospitals in Illinois. The spatial accessibiilty is measured by the use of an enhanced two-step floating catchment area (E2FCA) method (Luo & Qi, 2009), which is an outcome of interactions between demands (i.e, # of potential patients; people) and supply (i.e., # of beds or physicians). The result is a map of spatial accessibility to hospital beds. It identifies which regions need more healthcare resources, such as the number of ICU beds and ventilators. This notebook serves as a guideline of which areas need more beds in the fight against COVID-19.

To view accessibility measures updated daily, check out: https://wherecovid19.cigi.illinois.edu/

### What's Inside

A quick explanation of the components: 

* `Data` contains all of the data necessary for calculations:
  * `Chicago_Network.graphml`/`Illinois_Network.graphml` are GraphML files of the OSMNX street networks for Chicago and Illinois respectively.
  * `GridFile/` has hexagonal gridfiles for Chicago and Illinois
  * `HospitalData/` has shapefiles for the hospitals in Chicago and Illinois
  * `IL_zip_covid19/COVIDZip.json` has JSON file which contains COVID cases by zip code from IDPH
  * `PopData/` contains population data for Chicago and Illinois by census tract and zip code.
  * `Result/` is where we write out the results of the spatial accessibility measures
  * `SVI/`contains data about the Social Vulnerability Index (SVI)
