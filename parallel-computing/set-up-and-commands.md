#Set up and commands

Some basic commands and set-up to access RWTH's cluster network.

### Login
* Basic secure shell is `ab123456@login18-1.hpc.itc.rwth-aachen.de` with endpoints differing depending on the type of architecture/hardware you want to access.

### Transferring Files
* local-to-cluster is `scp ~/file.zip ab123456@login18-1.hpc.itc.rwth-aachen.de:`
* Remote sync is similar to git in that it syncs the remote server with your local copy. `rsync -a ab123456@login18-1.hpc.itc.rwth-aachen.de:from_cluster ~/folder`

### FastX
* commands are generally `module load GRAPHICS`, `module load paraview`, then `paraview` to view the 3d graphics program for FEM.