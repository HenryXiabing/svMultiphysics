# svMultiphysics Workflow

## Step 1: CFD with Rigid Wall
Run 'J_PF_01-rigid.slurm' in folder:
'98_2A_CoA7\01-rigid'

## Step 2: Wall Prestress
Use the pressure and velocity from the last VTU file 
(diastoic time point) of Step 1 to run:
'02-1-prestress' in folder:
'98_2A_CoA7\02-deform-ale\02.1-prestress'

## Step 3: FSI ALE
Use the flow from Step 1 and wall prestress from Step 2 
to conduct the FSI simulation.

### Known Issues
Step 3 often fails with errors such as:

FS 26-1  1.733e+01  [0 1.000e+00 1.159e+00 9.973e-05]  [385 -5 82]  
MS 26-1  1.743e+01  [0 1.000e+00 5.530e+02 9.872e-05]  [138 -92 82]  
FS 26-2  5.235e+01  [17 7.642e+00 8.854e+00 1.194e-02]  !30200 0 100!  
WARNING: The linear system solution has not converged  
ERROR: NaN detected in RCR integration
