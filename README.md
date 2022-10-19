# preprocessingCode
MATLAB scripts and functions for preprocessing behavioral and neural data from reaching experiments. This repo should be where we share preprocessing stuff for basically everything that happens after synchronization and before data analysis.

# Currently implemented stuff

Simple task and kinematic processing:

wrapper_preprocessTaskAndKinematicData_choking is a script where you can pass in lists of saved .mat files with synchronized data and folders with task data and get out processed task data. It calls pp_preprocessTaskAndKinematicData_choking, which processes the raw task data to extract relevant info (i.e., smoothed/upsampled kinematics, trial labels for target direction and reward, etc.). For tasks with parameters beyond reward and target (i.e., target size tasks, focus task), pp_preprocessTaskAndKinematicData_choking will probably need to be expanded copied -> adapted.

# Other things to implement and include here

Other things to go here:
- Analog data processing
  - EMG, EKG, eye - probably align to trial, normalize if needed (i.e. pupil, EMG)
- Neural data processing
  - initial processing first, like alignment
  - further processing later, like artifact detection, unit IDing across days, and stitching preprocessing

Overall, stuff will probably fall into 3 steps: (1) initial processing to get raw data in a usable form, (2) early preprocessing that extracts things relevant for all tasks from this data (i.e., behavioral metrics, unit identification, general artifact removal, maybe stitching?), (3) more specific experiment-specific processing and analysis
