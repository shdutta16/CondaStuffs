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
