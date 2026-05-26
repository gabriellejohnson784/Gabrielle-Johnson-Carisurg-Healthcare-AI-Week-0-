# Gabrielle-Johnson-Carisurg-Healthcare-AI-Week-0-
A collection of the daily week 0 assignments 

## Assignment 1 Data Cleaning (Gender Column)
  In Assignment 1, I was tasked with cleaning the gender column of the given dataset. During this process, I encountered some of the challenges that arise when dealing with columns containing inconsistent and varying values. Additionally, the questions at the end of the tutorial encouraged me to think beyond the traditional binary view of gender and consider how to create a solution capable of handling non-binary and other unexpected values in the future. To address this, I applied techniques such as value mapping, and one-hot encoding, which I had previously learned, to create a cleaner and more scalable gender column suitable for both present and future cleaning. Initially, I standardized the dataset by mapping female values to 0 and male values to 1 so the data could be represented numerically, while also exploring one-hot encoding as a more flexible and scalable approach since it can better accommodate additional gender categories if introduced later on.

## Assignment 2 Data Cleaning (MAP)
In Assignment 2 I worked alongside Tianna, Josiah-John, Ansarah and Shari to clean the MAP column of the dataset. During this process, we learnt that MAP is derived from both the SBP and DBP values, so it was important to clean those columns first before recalculating MAP. This helped to prevent inaccurate MAP values that could result from dirty or inconsistent data.

  ### Path Way to Cleaning MAP
  1. We converted the SBP and DBP columns to numeric values, checked them against valid clinical ranges, and replaced any invalid entries with missing values. Rather than deleting rows with missing data, we used the median to impute missing SBP and DBP values because the dataset was skewed and the median is less affected by extreme values.
  2. After cleaning both columns, we recalculated MAP using the formula MAP = \frac{SBP + 2(DBP)}{3}. We chose to recalculate MAP instead of relying on the original MAP column because the original values may have been generated using unclean SBP and DBP data. This made the final MAP values more accurate and consistent.
  3. Finally, we performed a validation check and found that both SBP and DBP had 0 out-of-range values and 0 missing values. MAP also had 0 missing values, with only 1 value slightly below 40 mmHg. We decided to keep this value because it was recalculated from valid SBP and DBP values, meaning it could realistically represent a critically ill patient rather than a data entry error.
  
This assignment was a great collaboration effort with my peers in this program. We were all able to readily provide solutions and had extensive, productive and thought-provoking discussion on the varying methods we chose;with this we were all able to come together and choose the solution we though best fit the problem. 

## Assignment 3- Data Visualization
In Assignment 3, I was tasked with visualizing the data we had been working on for the past two days. Before beginning the visualizations, I ensured that the data was cleaned so that the graphs would be based on accurate and reliable information.
  ### Histogram -Respiratory Rate 
  To examine the distribution of respiratory rates, I decided that a histogram would be the most appropriate graph since respiratory rate is a continuous variable. Clinical reference lines were added at 12 and 20 breaths per minute to represent the normal respiratory rate range and help identify patients whose breathing rates fell outside normal limits. Most patients were clustered within or slightly above the normal range, although elevated respiratory rates were observed.
  ### Scatter Plot- FiO2 and Respiratory Rate 
  Next, I explored the relationship between FiO₂ and respiratory rate to see how breathing rates varied across different oxygen concentrations. Reference lines at 12 and 20 breaths per minute were again included to highlight the normal respiratory rate range and make it easier to identify abnormal breathing patterns at different FiO₂ levels. However, to my surprise, the graph showed that respiratory rates varied widely across all oxygen levels, suggesting that there was no strong relationship between FiO₂ and respiratory rate; as there were many patients who had optimum FiO2 levels but still had alarmingly high respiratory rates.
  
## Assignment 4 - GCS 
Due to my unfamiliarity with the GCS vital sign, I decided that this would be a good time to explore what it means and its significance within the triage system. According to the Cleveland Clinic (2023), GCS stands for the Glasgow Coma Scale. It is a system used by healthcare
providers to determine how conscious a person is, or how deeply they may be in a coma, based on eye, speech, and movement responses. However, it is important to note that the GCS is most significant in patients with neurological
impairment. Therefore, while the GCS should not be used on its own to prioritise patients, it remains extremely valuable within the triage process, particularly from a neurological standpoint.

## Assignment 5- SpO2
During research on constructing a scatter plot for FiO2 on Assignment 3, I encountered another vital sign that is closely related to FiO2 and frequently used alongside it: SpO2. SpO2 stands for peripheral oxygen saturation and measures the percentage of oxygen carried in the blood
compared to the blood’s maximum oxygen-carrying capacity.

The World Health Organisation (2021) summarised below how to interpret the readings of the SpO2 percentage.
1. SPO2 ≥ 94% with no emergency signs (chest pain, dyspnoea, shortness of breath, altered
mental status)- normal reading. Continue monitoring at home
2. SP02 ≤ 94%- patient requires hospitalisation for monitoring and further management.
3. SP02 ≤ 90% is a medical emergency and requires referral to a health facility with an intensive
care unit or high dependency unit.

SpO2 should not be treated as a standalone variable that solely determines whether a patient requires immediate care. Like all other vital signs, it must be interpreted alongside additional vital signs. Nevertheless, incorporating SpO2 into triage assessments can provide healthcare workers with significant insight into a patient’s respiratory condition and help prioritise patients who may require urgent medical attention.

## Assignment 6 -Triage Pseudocode
In Assignment 6, I undertook the daunting task of creating an emergency triage pseudocode. To reduce complications, I broke down the process into key factors that I believe should be considered, along with additional factors identified during my research.

To triage patients effectively, I considered not only the patient’s condition, but also the hospital’s available resources. For example, this includes the number of doctors and nurses available to treat patients, the number of available beds, and other resources needed for care.This is important because triage is not only about identifying how sick a patient is, but also about deciding how care should be prioritized when resources are limited.
I also examined patient's pre-existing conditions, alongside their vital signs, to help define different risk categories, such as critical, high-risk, urgent, low-risk, and expectant cases - where the chance of survival may be extremely limited even with intervention. This would further assist in prioritising patients.

To achieve the best possible results, I attempted to combine elements from several existing triage systems used globally. I relied heavily on online research papers to guide the design process. Although I am not yet fully confident with the technicalities of the pseudocode, I attempted to encapsulate and provide a high-level interpretation of what I intend and hope the system will accomplish within the triage process.


