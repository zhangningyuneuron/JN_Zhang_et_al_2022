# Journal of Neurosci_Zhang_et_al_2022
Data &amp; Code for Zhang et al. 2022, published in Journal or Neuroscience https://doi.org/10.1523/JNEUROSCI.0619-22.2022

CODE: the zip.file contain 2 main functions: contest_v2 and egoTEST_v2, and their dependencies. Descriptions below: 

%% contest_v2  function for analysing directional cells in different environments (e.g.multicompartment maze, 2-box and 4-box)
%     A function for analysing the data collected from the 1-box,2-box and 4-box (multicompartment maze)
%     This uses an 'sdata' structure, produced by custom-built MATLAB code to analyze raw data (see https://www.nature.com/articles/s41467-020-14611-7)
%     It can run on a single tetrode and cluster:
%     contest(out_name,tetrodes,clusters) 
%     This function allows the user to specify the maze boundaries and trial order
%     with this information we can divide data between the different compartments
%     and compare tuning curves in this way. The output of the functions
%     are specified in contest_v2. 

%% egoTEST_v2  function for analysing egocentric boundary tuning in different environments (e.g.multicompartment maze, 2-box and 4-box)
%     This function should be run following contest_v2 (specifies maze frame/boundaries)
%     This function mainly replicates the analysis reported in:
%     Alexander et al. (2019) Egocentric boundary vector tuning of the retrosplenial cortex (http://dx.doi.org/10.1101/702712)
%     to test for egocentric boundary cell coding. Most of the analysis is placed in the sdata structure. 
