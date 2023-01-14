# Energy A.I. Hackathon 2023

## Hosts: [Prof. Michael Pyrcz](https://twitter.com/GeostatsGuy) and [Prof. John T. Foster](https://twitter.com/johntfoster)

### Architects: [Elnara Rustamzade](https://www.linkedin.com/in/elnara-rustamzade-779396162/) and [Ruoyu Wang](www.linkedin.com/in/ruoyu-wang1)

### Sponsors: [Prof. Jon Olson](https://twitter.com/ProfJEOlson), and the [Hildebrand Department of Petroleum and Geosystems Engineering](https://twitter.com/UT_PGE)

### Organization and Student Engagement: Gabby Banales, Sara Hernando and Tracey Wilson

___

### Energy A.I. Problem Description 

**Goal**: Develop a data analytics and machine learning workflow in Python to:

1. classify whether an Artifical Lift ESP will **"fail" or "not fail" within 30 days**.
2. predict the **status of the test cases**.
 
#### Background

In order to prevent the production loss caused by Electronic Submersible Pump(ESP) failures in Artifical Lifts, we challenge the Energy A.I. hackathon teams of The University of Texas at Austin, engineering and science students to build a data-driven model to detect when an ESP is nearing failure.

This will require:

* data analysis and evaluation of multiple data sources and a variety of features
* feature engineering including feature selection/transformation/imputation
* integration of domain expertise at every step
* selection, training and tuning robust machine learning prediction models  

<!-- This data-driven approach will replace the conventional engineering and geoscience approach:

* characterizing and modeling the subsurface
* physics-based fluid flow simulations -->

___

### Available Data Files Inventory

You have the following available data:

#### Well/Pump Data

* **wellData.csv** - data on 166 unique pumps installed on 146 wells. For example, if an ESP fails and a new ESP is installed, there will be two rows for one well - one for ESP_1 and another for ESP_2.

The features include:

* **AL_Bottom_Depth (ft)** - the depth at which an ESP is landed
* **ESP_Pump_Stages** - the components that impart a pressure rise to the fluid
* **DLS_Critical (degree/100ft)** - critical dogleg severity; until a dog-leg reaches this threshold value, no drill stem fatigue damage occurs
* **ESP_Motor_Frequency_Rating (Hz)** - rated frequency of the motor
* **ESP_Motor_Current_Rating (A)** - rated current of the motor
* **ESP_Motor_Voltage_Rating (V)** - rated voltage of the motor
* **DLS_at_Set_Depth (degree/100ft)** - dogleg severity at the depth of the ESP
* **Failure_Type** -  ESP failure type; can be "electrical", "pump", or "tubing"
* **Failure_Type_Detail** - detailed ESP failure type; can be "motor", "penetrator", "stage", etc
* **Status** -  ESP status; can be either "failed", "active", or missing. Missing status indicates that an ESP is a test case

#### Daily Data

* **dailyData.csv** - dynamic data collected daily. For each well, there will be a row of data for each day that the ESP is installed.

The features include:

* **OIL (bbl)** - oil production 
* **GAS (SCF)** - gas production
* **WATER (bbl)** - water production
* **DOWN_TIME_HOURS** - the amount of time the well was shut for per day
* **Oil_Intake (bbl)** - the amount of oil that enters the system
* **Water_Intake (bbl)** - the amount of water that enters the system
* **Gas_Intake (SCF)** - the amount of gas that enters the system
* **Liquid_Intake (bbl)** - the amount of liquid that enters the system
* **Gas_Saturation_at_Intake** - ratio of the amount of gas entering the system to the total volume
* **Gas_Saturation_at_Discharge** - ratio of the amount of gas leaving the system to the total volume
* **Gas_Separator_Efficiency** - ratio of the reduced volume of free gas to the volume before entering the separator
* **Pump_Delta_Pressure (psi)** - the difference between discharge and intake pressure
* **Power_Ratio** - ratio of pump power to drive power
* **Power_Difference (psi)** - the difference between drive and pump power


Comments: 

* all the well names are masked (replaced with simple indices).
* NaN in the file indicate missing data.


___

### Required Hackathon Submissions

<span style='color:red'>Links below will be changed when all files are pushed to github</span>

By January 22 at noon each team must submit:

* **Solution Table** - a .csv file with your predictions for the **test cases** using the template given in [Sample_Submission.csv](Sample_Submission.csv) in this directory.

    * the file must be named 'solution.csv' with final values in a commit and then pushed to Github (folder [scoring/submission](https://github.com/PGEHackathon/data/tree/master/scoring/submission)) for the automated scoring.


* **Python Workflow and Associated Files** - committed to this repository with the workflow as a Jupyter Notebook .ipynb file along with all data files required to reproduce your team's solutions. The submitted workflow Jupyter Notebook should follow the format of the provided template [Hackathon_ProjectTemplate](https://github.com/PGEHackathon/resources/blob/main/Hackathon_ProjectTemplate.ipynb) for enhanced workflow communication and code readibility.

    * the file must be named 'xxxx.ipynb' and pushed to GitHub (folder [scoring/workflow](scoring/workflow)  for review and scoring (for code readability) by the hackathon architects, , where **xxxx** is your team name.


* **Presentation** - a PowerPoint slide deck .PPTX file for your team's final presentation to our judges. The submitted presentation should follow the format of the provided example presentation [Hackathon_PresentationTemplate](https://github.com/PGEHackathon/resources/blob/master/Hackathon_PresentationTemplate.pptx).

    * the file must be named 'xxxx.pdf' and pushed to GitHub (folder [scoring/presentation](scoring/presentation) for review by the judges, where **xxxx** is your team name.

The Workflow, Presentation submission templates and the results submission template are in the [PGEHackathon/resources](https://github.com/PGEHackathon/resources) repository.

