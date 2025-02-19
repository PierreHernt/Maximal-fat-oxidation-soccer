# Maximal Fat Oxidation and High-Intensity Running Performance in Elite Players

## ABSTRACT
* **Purpose** :  Maximal fat oxidation rate (MFO) is considered an important determinant of athletic performance in endurance sports, but its impact on physical performance in team sports, especially soccer, remains poorly understood. This study examined the possible associations between MFO and match running performance in elite soccer players, aiming to assess the importance of MFO in match performance compared to other physical qualities traditionally targeted by physical trainers.
* **Methods** : During the pre-season, 41 youth elite soccer players performed a maximal and a fasted submaximal graded exercise tests on a treadmill to determine peak oxygen uptake (VO2max) and MFO, respectively. Additionally, vertical and horizontal force-velocity-power profile were obtained for each soccer player. Match running performance was measured by a global positioning system (GPS) over a competitive season. 
* **Results** :  Based on the weight of each variable obtained from 100 bootstraps on our regression trees, VO2max was identified as the most important variable to estimate total distance, F0 and Pmax to estimate sprint distance, and MFO to estimate high-intensity running (> 15 km·h-1). Players exhibiting \dot{V}O2max greater than 55.6 ml·min·kg-1 covered more distance than others (P<0.001), and players with a MFO greater than 0.73 g·min-1 covered more high-intensity distance (P<0.001).
* **Conclusion** : These findings support that maximal fat oxidation plays an important role in high-intensity running performance during soccer games. Optimizing physical performance and endurance in soccer requires a holistic training approach that should target both lower limb explosiveness, aerobic power, and fat oxidation, recognizing the multifaceted nature of high-intensity effort.  

* **Keywords**: fat oxidation, exercise physiology, football, metabolic profile, anaerobic threshold, performance


## DATASET
This study utilized two main datasets: 

**RAW_DATA.csv** : This dataset contains the non-standardized GPS data used to observe the physical performance of players during matches. It also includes all the physical and physiological variables collected during the study.

Variables:
* ID 
* Poste
* MFO (g/min)
* VO2max (ml/min/kg)
* Horizontal F0 (N/kg)
* Horizontal V0 (m/s)
* Horizontal Pmax (W/kg)
* Vertical F0 (N/kg)
* Vertical V0 (m/s)
* Vertical Pmax (W/kg)
* Total Distance (m)
* Low Speed Running (0-14.99 km/h) (m)
* Moderate Speed Running (15-19.99 km/h) (m)
* High Speed Running (20-24.99 km/h) (m)
* Very High Intensity Running (> 20 km/h) (m)
* Sprinting (> 25 km/h) (m)
* High Intensity Running (> 15 km/h) (m)


**STANDARDIZED_DATA.csv** : This dataset contains the standardized data used in the study to observe the impact of physiological variables on physical performance during matches.

Variables:
* ID 
* Poste
* MFO (g/min)
* VO2max (ml/min/kg)
* Horizontal F0 (N/kg)
* Horizontal V0 (m/s)
* Horizontal Pmax (W/kg)
* Vertical F0 (N/kg)
* Vertical V0 (m/s)
* Vertical Pmax (W/kg)
* Total Distance (Z-score)
* High Speed Running (20-24.99 km/h) (Z-score)
* Sprinting (> 25 km/h) (Z-score)
* High Intensity Running (> 15 km/h) (Z-score)

## CODE 

**SIMPLE_TREE** :  A simplified regression tree model with one split. The results of this model are illustrated in our figures. The main split threshold of the tree was selected to segment individuals based on the physiological variable most associated with our GPS variable of interest.

**VARIABLES_IMPORTANCES** : To analyze the impact of various physiological variables on the measured GPS data, regression trees were used, and their importance was assessed using 1000 bootstrap samples. This method aims to provide stable estimates of variable importance, expressed as mean ± SD. 

