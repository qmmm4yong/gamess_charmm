
This repositoy is about the containarized interface between CHARMM and GAMESS programs.

Due to licensing demands for both GAMESS and CHARMM, the container
itself is not on this repository. One must first obtain the license
for CHARMM and GAMESS programs, both free of charge and then write to
milan@cmm.ki.si to obtain access to the container itself.

In the future I will provide a protoype container that can compile
CHARMM and GAMESS by the users themselves, but for now I make one
myself and put it on a private link.

The repository has 3 prototype jupyter notebooks:

1.   You can do a simple QM/MM calculation with the files from
     CHARMM-GUI. You just need to specify the names of the files and
     what part of the system you want to use QM for. Then the jupyter
     notebook will make a QM/MM file for you. You can run this file on
     a computer with many processors using any batch system you like.

    Currently the selection of QM atoms is specifed as a string, but
    in the future it can be improved to be specified by picking QM
    atoms with the mouse clicks.
    
    Use simulation notebook for this.
    
   
2. Setup for the Replica Path calculations. This is an efficient
   implementation because the job can be executed in parallel/parallel
   setup. This means that each replica is a separate job, executed in
   parallel. Eg one has 30 replicas and each replica takes 30
   processors, that means the whole calculation can be run on 900
   processors.

    Use path notebook and specify number of replicas and the names of
    reactant and product structures. The structures must have the same
    PSF file.

3. Setup for vibrational analysis: calculation of QM/MM frequencies
   This is a time consuming calculation but can be improved to become
   very efficient parallel calculation, using more than 1000
   processsors. Currenty this is not yet implemented.
   
   Use vibran notebook. Specify structure which mst be minimized
   (either minimum or transition state) befor frequency calculation.
   
   For this we use 2 notebooks: vibran, freq. Vibran caclulates the
   Hessian and saves it on a specified file. Vibrational commands are
   added by the notebook.
   
   The second shows the frequencies and allows user to specify which
   vibrational mode the user want to see in an animation. This
   animations are prodcuced quickly so one can explore several in a
   short time.
   
   
   
   
