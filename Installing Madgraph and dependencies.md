## Installing Madgraph and dependencies

1. **Prepare the system**
   
   First of all, it is necessary to get the system working with the newest update, so we will run:
   
   ```bash
   sudo apt update && sudo apt upgrade
   ```
   
   It is important to accept using (y).
   
   Also, it is important to have a `Fortran` compiler installed,  this is done via:
   
   ```bash
   sudo apt install gfortran -y
   ```

2. **Install MadGraph**
   
   We now install the version of MadGraph we will use, for this instructions, we will use the verison  3.3.1. Thus, the installation can be made form the terminal in the desired forder like:
   
   ```bash
   sudo apt install wget
   wget https://launchpad.net/mg5amcnlo/3.0/3.3.x/+download/MG5_aMC_v3.3.1.tar.gz
   ```
   
   ```bash
   tar -xvf MG5_aMC_v3.3.1.tar.gz
   ```
   
   As the binaries are already compiled, the file extraction should lead to a complete MG5 installation.    We can check if ti works via:
   
   ```bash
   ./MG5_aMC_v3_3_1/bin/mg5_aMC
   ```
   
   And the MadGraph insterface should be visible.

3. **Installing Pythia**
   
   Within the ```mg5``` interface, we can install pythia via:
   
   ```bash
   MG5_aMC>install pythia8
   ```
   
   Then he is going to ask whether we want to install ```LHAPDF```. Please answer yes.
   
   When no flow in the terminal is running, please open another in the folder where madgraph was installed (for example ```~/Research/MADGRAPH```) and type:
   
   ```bash
   cd ./MG5_aMC_v3_3_1/bin
   tail -f ./MG5_aMC_v3_3_1/HEPTools/pythia8/pythia8_install.log
   mg path /home/debguane/Documents/RESEARCHING/ParticlesTurkey/MADGRAPH/MG5_aMC_v3_3_1
   
   ```
   
   You should see a ```Finished PYTHIA8 installation``` at the end of the installation.

4. **Installing MadAnalysis5**
   
   In order to install MadAnalysis5, you should go back to the terminal where madgraph is running and type:
   
   ```bash
   MG5_aMC>install MadAnalysis5     
   ```
   
   If this doesnt works, it is probably due to incompatibilities with the python version in the path. I recommend then to go with the old MadAnalysis verion as:
   
   ```bash
   mG5_aMC>install MadAnalysis4
   
   
   ```

Now, we are ready to install other dependencies such as ExRootAnalysis and Delphes. But for this, it is necesary to have an especific Root-Frameworok verision installed. We attack this issue in the next steps.


