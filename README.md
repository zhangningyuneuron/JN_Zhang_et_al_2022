# Journal of Neurosci_Zhang_et_al_2022
Data &amp; Code for Zhang et al. 2022, published in Journal or Neuroscience https://doi.org/10.1523/JNEUROSCI.0619-22.2022

**CODE: Code zip.file contains 2 main functions of analyses: contest_v2 and egoTEST_v2 and their dependencies**

%% contest_v2  functions for directional cells in different environments 
%    This function is for analysing the data collected from the 1-box,2-box and 4-box (multicompartment maze), especially the directionality and symmetry. This builds on an 'sdata' structure, produced by custom-built MATLAB code to analyze raw ephys data (see https://www.nature.com/articles/s41467-020-14611-7). This function can run on a single tetrode and cluster: contest(out_name,tetrodes,clusters). Importantly, this allows the user to specify the maze boundaries and trial order, with this information we can divide data between the different (sub)compartments and compare tuning curves in this way. The output of the functions are specified in contest_v2. 

%% egoTEST_v2  function for analysing egocentric boundary tuning in different environments (e.g.multicompartment maze, 2-box and 4-box)
%     This function should be run following contest_v2 (specifies maze frame/boundaries). This function mainly replicates the analysis reported in: Alexander et al. (2019) Egocentric boundary vector tuning of the retrosplenial cortex (http://dx.doi.org/10.1101/702712). We aimed to test for any egocentric boundary cell coding that might be embedded in our dataset. Most of the analysed results is placed in the sdata structure (see below). 

**DATA: The dataset.zip consists of three .mat files.**
Each of which contains a MATLAB structure (named mdata) that summarises the analysed data of different experiments
- All_HD cells: all 102 HD cells recorded from the 2box (mdata_2box) and 4box (mdata_4box) experiments, 1box trials were alse included.  
- All_BD cells: all 48 BD cells recorded from the 2box (+ 1box trials) 
- All_TD cells: all 67 TD cells recorded from the 4box (+ 1box trials) 

%%     The mdata structures should be easy to navigate but here are some pointers:
%         Recordings consist of onefold environments (e.g., circular arena, at least 2 trials, usually trial 'a' and 'g') that flank the multi-fold environments (at least 5 tirals, usually trial 'b'-'f'). Cell data such as spikes are saved in fields named using a unique cell identifier (uci). This consists of the rat, date, tetrode and cluster. These can be generated in loops etc. To refer to a specific unit, uci = rat_num, date, tetrode_num, cluster_id.  

%%     For each single unit, you can find the several analysed features (column headers are self-explanatory), such as cluster quality, waveform information of each unit, shuffle data of that cell, HDtuning in the overall environment and within each subcompartment, the symmetry scores, and the results from egocentric analyses etc. 

%%  Refer to our paper and code mentioned above for more details. 
