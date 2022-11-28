# Journal of Neurosci_Zhang_et_al_2022
Data &amp; Code for Zhang et al. 2022, published in Journal or Neuroscience https://doi.org/10.1523/JNEUROSCI.0619-22.2022

CODE: the Code zip.file contain 2 main functions of analyses: contest_v2 and egoTEST_v2, and their dependencies. Descriptions below: 

%% contest_v2  function for analysing directional cells in different environments (e.g.multicompartment maze, 2-box and 4-box)
%     A function for analysing the data collected from the 1-box,2-box and 4-box (multicompartment maze)
%     This uses an 'sdata' structure, produced by custom-built MATLAB code to analyze raw data (see https://www.nature.com/articles/s41467-020-14611-7)
%     It can run on a single tetrode and cluster:
%     contest(out_name,tetrodes,clusters) 
%     This function allows the user to specify the maze boundaries and trial order with this information we can divide data between the different compartments and compare tuning curves in this way. The output of the functions are specified in contest_v2. 

%% egoTEST_v2  function for analysing egocentric boundary tuning in different environments (e.g.multicompartment maze, 2-box and 4-box)
%     This function should be run following contest_v2 (specifies maze frame/boundaries)
%     This function mainly replicates the analysis reported in:
%     Alexander et al. (2019) Egocentric boundary vector tuning of the retrosplenial cortex (http://dx.doi.org/10.1101/702712)
%     with an aim to test for any egocentric boundary cell coding that might be embedded in our dataset. Most of the analysed results is placed in the sdata structure. 

DATA: The dataset.zip consists of three Matlab .mat files, each of which contains a structure (named mdata) that summarises the data recorded from different experiments:
- All_HD cells: all 102 HD cells recorded from the 2box (mdata_2box) and 4box (mdata_4box) experiments. 
- All_BD cells: all 48 BD cells recorded from the 2box 
- All_TD cells: all 67 TD cells recorded from the 4box 

%     The mdata structures should be easy to navigate but here are some pointers:
%         Recordings consist of onefold environments (e.g., circular arena, at least 2 trials, usually trial 'a' and 'g') that flank the multi-fold environments (at least 5 tirals, usually trial 'b'-'f').
%         Cell data such as spikes are saved in fields named using a unique cell identifier (uci) 
%         This consists of the rat, date, tetrode and cluster. These can be generated in loops etc
%         if you know which cell you want like this:
%         uci = ['r' rat_num '_' date '_t' tetrode_num_as_string '_c' cluster_num_as_string];

%     For each cell you can find the several analysed features (column headers are self-explanatory), such as cluster quality,  
%         waveform information of each unit, shuffle data of that cell, HDtuning in the overall environment and within each
%         subcompartment, egocentric analyses etc. Refer to the code for more details. 
