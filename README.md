# Simulation-Survival-Data-in-R
#===============================================================================
#                     F R E Q U E N T I S T I C
#
#                       S I M U L A T I O N 
#
#                     SIMULATE SURVIVAL DATA   
#===============================================================================
#   The example is a comparison of three different methods for 
#   estimating the hazard ratio in a randomised trial with a survival outcome.
#   Consider the proportional hazards model, 
#   where we have the hazard rate 
#   (event rate at time t conditional on survival until at least time t) 
#   for the ith patient
#   hi(t) = h0(t) exp(Xi𝜃),
#   In our simulation study true β = - 0.5. 
#   So the hazard ratio is exp(β) = 0.6065307.
#   The interpretation of the hazard ratio of 0.607 is that 
#   patients with Treatment (x=1) die at about 0.607 times than 
#   the patients with Treatment (x=0).Another way of expressing 
#   the hazard ratio that can be more meaningful to subject matter 
#   scientists is to describe it as a percentage increase/decrease 
#   over the null value of 1.In our simulation study one would say 
#   that the death rate among patients with Treatment 1 (x=1) 
#    is (1-0.607)100% = 39.3% smaller than among patients with 
#    Treatment 0 (x=0) throughout the study
#    We generate random numbers from Weibull distribution with scale 
#    parameter gamma = 1 which is the same as exponential distribution 
#    and random numbers from weibull with gamma =1.5.We regress them to 
#    three different proportional hazard models:
#    1)Exponential 
#    2)Weibull 
#    3)Cox 
#
#    Then we check the bias,coverage,model standard error,relative standard error,replative precision 
#    and other performance measures in R.
