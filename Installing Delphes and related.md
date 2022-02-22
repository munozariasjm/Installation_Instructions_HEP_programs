## Installing Delphes and related

Once you have completed the procedure to install Root-Framework, we are ready to install Delphes.

Please begin by opening a new MadGraph session in a recently opened terminal.

1. **Installing ExRootAnalysis**
   
   In order to let Delphes that root is available, it is necesary to add ExRootAnalysis. It is as simple as typing:
   
   ```bash
   MG5_aMC>install ExRootAnalysis 
   ```
   
   You should see a happy message with: `Installation succeeded`.

2. **Installing Delphes**
   
   We can finally proceed to install Delphes uising the same MadGraph session. So do:
   
   ```bash
   MG5_aMC>install Delphes
   ```

3. **Checking the installation**
   
   To finally check if it worked, we can generate a foo process:
   
   ```bash
   MG5_aMC>generate e+ e- > a a
   
   MG5_aMC>output foo_try
   
   MG5_aMC>launch foo_try
   ```
   
   We can finally turn on both Delphes and Pythia and see:
   
   ```bash
   The following switches determine which programs are run:
   /=================== Description ===================|================== values ===================|===== other options =====\
   | 1. Choose the shower/hadronization program        |        shower = Pythia8                     |     OFF                 |
   | 2. Choose the detector simulation program         |      detector = Delphes                     |     OFF                 |
   | 3. Choose an analysis package (plot/convert)      |      analysis = MadAnalysis4                |     OFF|ExRoot          |
   | 4. Decay onshell particles                        |       madspin = OFF                         |     ON|onshell|full     |
   | 5. Add weights to events for new hypp.            |      reweight = OFF                         |     ON                  |
   \===========================================================================================================================/
   
   ```

### Then... Happy physics!
