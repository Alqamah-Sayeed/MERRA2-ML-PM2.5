# **MERRA2-ML PM2.5 - A global long-term hourly dataset**

In the MERRA2-ML PM2.5 dataset, the Modern-Era Retrospective analysis for Research and Applications, Version 2 (MERRA2) as the base model was used. The meteorological parameters and aerosol components (particulate speciation) from MERRA2 were used and collocated with surface measurements. The collocated datasets were then used to develop ensemble machine learning (ML) algorithms with MERRA2 data fields as input and ground measurements (from over 5000 monitors) of PM2.5 as a target parameter. The ML architecture consists of multi-layers of convolutional neural network (CNN) and was trained on MERRA2 (meteorology and particulate speciation) as inputs and surface measured PM2.5 as the target variable. Different ML models were trained based on the dominating species from a particular grid. Figure 1 shows the model architecture, where 5 different CNN models were used to train an ensemble model for global PM2.5 estimations. The final, hourly PM2.5 mass concentration (micro g/m3) for 2000 to 2023 is derived using an ensemble ML model (Gupta et al., 2021; Gupta & Sayeed, 2024; Sayeed et al., 2022, 2023, Gupta et al., 2024- in prep). 
![image](https://github.com/Alqamah-Sayeed/MERRA2-ML-PM2.5/assets/163429432/8ea433de-08a3-4ce9-aff6-e06913cf3e1f)

Figure 1: The algorithm for estimation of global hourly surface PM2.5 concentrations.

The dataset consists of two parameters “MERRA2_CNN_Surface_PM25” and “QFLAG”. MERRA2_CNN_Surface_PM25 is a 3-dimensional variable (time, lat, lon) and has surface PM2.5 concentrations in microgram/m3. The time dimension starts at 0:30 UTC and ends at 23:30 UTC with hourly frequency. The lat (latitude) is from 90 deg S to 90 deg N with 0.5 deg spatial resolution and lon (longitude) is from 180 deg W to 180 deg E with 0.625 deg patial resolution. QFLAG denotes the quality of data at each grid point where 4 is the highest quality and 1 is the lowest quality. 

**PI: Pawan Gupta (pawan.gupta@nasa.gov, GSFC)**

**Lead Scientist: Alqamah Sayeed (alqamah.sayeed@nasa.gov, MSFC)**




# References:
**Gupta, P., & Sayeed, A. (2024). GES DISC Mission Guides: HAQAST Global Hourly PM2.5. https://disc.gsfc.nasa.gov/datasets/MERRA2_CNN_HAQAST_PM25_1/summary**

**Sayeed, A., Lin, P., Gupta, P., Tran, N. N. M., Buchard, V., & Christopher, S. (2022). Hourly and Daily PM 2.5 Estimations Using MERRA‐2: A Machine Learning Approach. Earth and Space Science, 9(11), e2022EA002375. https://doi.org/10.1029/2022EA002375**

**Gupta, P., Zhan, S., Mishra, V., Aekakkararungroj, A., Markert, A., Paibong, S., & Chishtie, F. (2021). Machine Learning Algorithm for Estimating Surface PM2.5 in Thailand. Aerosol and Air Quality Research, 21(11), 210105. https://doi.org/10.4209/aaqr.210105**

Buchard, V., da Silva, A. M., Randles, C. A., Colarco, P., Ferrare, R., Hair, J., Hostetler, C., Tackett, J., & Winker, D. (2016). Evaluation of the surface PM2.5 in Version 1 of the NASA MERRA Aerosol Reanalysis over the United States. Atmospheric Environment, 125, 100–111. https://doi.org/10.1016/j.atmosenv.2015.11.004

Colarco, P., da Silva, A., Chin, M., & Diehl, T. (2010). Online simulations of global aerosol distributions in the NASA GEOS-4 model and comparisons to satellite and ground-based aerosol optical depth. Journal of Geophysical Research: Atmospheres, 115(D14). https://doi.org/10.1029/2009JD012820



Koster, R. D., Darmenov, A., & Silva, A. da. (2015, September 1). The Quick Fire Emissions Dataset (QFED): Documentation of Versions 2.1, 2.2 and 2.4. Volume 38; Technical Report Series on Global Modeling and Data Assimilation. https://www.semanticscholar.org/paper/The-Quick-Fire-Emissions-Dataset-(QFED)%3A-of-2.1%2C-on-Koster-Darmenov/f18b64dce3bc0f3384d0d8377b409597c5c665cb

Provençal, S., Buchard, V., da Silva, A. M., Leduc, R., & Barrette, N. (2017). Evaluation of PM surface concentrations simulated by Version 1 of NASA’s MERRA Aerosol Reanalysis over Europe. Atmospheric Pollution Research, 8(2), 374–382. https://doi.org/10.1016/j.apr.2016.10.009

Randles, C. A., Silva, A. M. da, Buchard, V., Colarco, P. R., Darmenov, A., Govindaraju, R., Smirnov, A., Holben, B., Ferrare, R., Hair, J., Shinozuka, Y., & Flynn, C. J. (2017). The MERRA-2 Aerosol Reanalysis, 1980 Onward. Part I: System Description and Data Assimilation Evaluation. Journal of Climate, 30(17), 6823–6850. https://doi.org/10.1175/JCLI-D-16-0609.1




