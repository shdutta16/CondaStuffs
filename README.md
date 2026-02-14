# CondaStuffs

## How to's
1. How to create a conda environment in a particular directory?
   ```
   conda create -p ./pioneer_env python=3.10
   ```

2. How to change the name-style so that the full path doesn't appear in the terminal?
   ```
   conda config --set env_prompt '({name}) '
   ```

3. How to update conda solver with libmamba (which is fast and takes less memory)?
   Run the following commands within the base environment:
   ```
   conda update -n base conda
   conda config --add channels defaults
   conda config --add channels conda-forge
   conda install -n base conda-libmamba-solver
   conda config --set solver libmamba
   ```

4. How to set and unset or run commands when conda environment is activated or deactivated?
   ```
   cd $CONDA_PREFIX
   mkdir -p ./etc/conda/activate.d
   mkdir -p ./etc/conda/deactivate.d
   touch ./etc/conda/activate.d/env_vars.sh
   touch ./etc/conda/deactivate.d/env_vars.sh
   ```
   When conda environment is activated (deactivated) ```.../activate.d/env_vars.sh``` (```.../deactivate.d/env_vars.sh```) is executed 
