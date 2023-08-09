# Cancer_Diagnosis

Problem statement:  Classify the given genetic variations/mutations based on evidence from text-based clinical literature.


Real-world/Business objectives and constraints:

No low-latency requirement.
Interpretability is important.
Errors can be very costly.
Probability of a data-point belonging to each class is needed.

Data Overview:
We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that  human experts/pathologists use to classify the genetic mutations. 
- Both these data files are have a common column called ID.

Data file's information:  training_variants (ID , Gene, Variations, Class), training_text (ID, Text)

Example DataPoint: training_variants

ID,Gene,Variation,Class

0,FAM58A,Truncating Mutations,1 


1,CBL,W802*,2 

2,CBL,Q249E,2 


ML Problem:

There are nine different classes a genetic mutation can be classified into => Multi class classification problem.

Machine Learing Objectives and Constraints
Objective: Predict the probability of each data-point belonging to each of the nine classes.
Constraints:
* Interpretability
* Class probabilities are needed.
* Penalize the errors in class probabilites => Metric is Log-loss.
* No Latency constraints.



