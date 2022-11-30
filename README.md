# Journal of Neurosci_Zhang_et_al_2022
Code for Zhang et al. 2022, published in Journal of Neuroscience https://doi.org/10.1523/JNEUROSCI.0619-22.2022

**CODE: Code zip.file contains 2 main functions of analyses: contest_v2 and egoTEST_v2 and their dependencies**

%% contest_v2  functions for directional cells in different environments. This function is for analysing the data collected from the 1-box,2-box and 4-box (multicompartment maze), especially the directionality and symmetry analyses. This builds on an 'sdata' structure, produced by custom-built MATLAB code to analyse raw ephys data (see Grieves et al. 2019 https://www.nature.com/articles/s41467-020-14611-7). This function can run on a single tetrode and cluster: contest(out_name,tetrodes,clusters). Importantly, this allows the user to specify the maze boundaries and trial order, with this information we can divide data between the different (sub)compartments and compare tuning curves in this way. The output of the functions are specified in contest_v2. 

%% egoTEST_v2  function for analysing egocentric boundary tuning in different environments (e.g.multicompartment maze, 2-box and 4-box). This function should be run following contest_v2 (specifies maze frame/boundaries). This function mainly replicates the analysis reported in: Alexander et al. (2019) Egocentric boundary vector tuning of the retrosplenial cortex (http://dx.doi.org/10.1101/702712). We aimed to test for any egocentric boundary cell coding that might be embedded in our dataset. Most of the analysed results is placed in the sdata structure (see below). 

%%  For more details, please refer to our paper. 
