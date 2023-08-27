### ICD therapy prediction - MSc Project Code
Implantable cardiovascular defibrillators (ICD) are small devices placed under the skin that monitor the heart and provide life-saving therapy in the form of shocks and electrical impulses to stop irregular beating of the heart (ventricular arrhythmias). The most common indication for ICD device implantation is heart failure. ICD therapies are life-saving, yet they are associated with decreased long-term survival and lower quality of life. Ideally, medical teams would be alerted about impending ventricular arrhythmias, providing an opportunity for close patient monitoring and timely preventative therapies. **Thus, this study aimed to develop advanced predictive machine learning models based on data collected daily by ICD devices. The resulting models demonstrated high accuracy in detecting patients at increased risk of ICD therapy.** Out of the monitored parameters, previous arrhythmias, patient activity levels, and the average heart rate were the most helpful in making predictions. The models must be tested on data collected in different centres before suggesting their use in clinical environments.

#### Notebooks (in order of importance):
**1. data_cleaning.ipynb** - notebook accepts patient files stored in individual .csv files and provides a cleaned dataframe with all the patients. 
**2. resampled_data_models.ipynb** - the main notebook with the best performing models. Data is resampled and logisitc regression, random forest, XGBoost and 1D-CNN models developed.  
**3. non-resampled_data_models.ipynb** - additional analysis notebook. Contains models trained on one sample per patient: XGBoost, 1D-CNN.
**4. extracted_data_models.ipynb** - additional analysis utilising extracted features. XGBoost, random forest models.
**5. data_visualisation.ipynb** - visualisation of time series data and exploration of variables in cases and controls. 

**File format:**
Please ensure that the .csv files containing patient data have these variables present:
**Features** = 'RV pacing impedance [ohm]', 'RV sensing amplitude (daily mean) [mV]', 'RV sensing amplitude (daily min.) [mV]', 'Daily shock lead impedance [ohm]', 'Right ven. pacing (RVp) [%]', 'VT1 monitoring episodes', 'VT1 therapy episodes', 'VT2 episodes', 'VF episodes', 'Episodes during temporary program', 'ATP in VT zones started', 'ATP in VT zones successful', 'ATP One Shot started', 'ATP One Shot successful', 'Shocks started', 'Shocks aborted', 'Shocks successful', 'Ineffective ven. max. energy shocks', 'Mean ventricular heart rate [bpm]', 'Mean ventricular heart rate at rest [bpm]', 'Patient activity [% of day]', 'ATP in VT/VF delivered', 'ATP One Shot delivered'.
**Time index** = 'Transmission received on (days)'
