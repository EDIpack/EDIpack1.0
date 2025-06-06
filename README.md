# EDIpack1.0: A *parallel* Exact Diagonalization solver for Quantum Impurity problems

This is the version 1.0 of EDIpack. 
A largely updated version can be found here: [EDIpack](https://github.com/EDIpack/EDIpack)

The 1.0 is a Lanczos based solver for generic quantum impurity models exploiting distributed memory MPI parallelisation. This software focuses on the solution in presence of $SU(2)$ or just $U(1)$-spin symmetry, thus including long range magnetic ordering and also arbitrary unit cells. 
The code is presented here [j.cpc.2021.108261](https://doi.org/10.1016/j.cpc.2021.108261). 

### Dependencies

The code is written around the SciFortran library. Dependencies are:   

* gfortran > 9.0.0 **OR** ifort  > 13.0
* cmake > 3.0.0    
* [MPI](https://github.com/open-mpi/ompi)
* [SciFortran](https://github.com/SciFortran/SciFortran)


### Installation

Installation is  available using CMake.    

Clone the repo:

`git clone https://github.com/EDIpack/EDIpack1.0 EDIpack1.0`

and from the just created directory make a standard out-of-source CMake compilation:

`mkdir build`  
 `cd build`  
`cmake ..`     
`make`     
`make install`   

The `CMake` compilation can be controlled using the following additional variables, default values between `< >`:   

* `-DPREFIX=prefix directory <~/opt/edipack/>` 
* `-DUSE_MPI=<yes>/no`  
* `-DVERBOSE=yes/<no> `  
* `-DBUILD_TYPE=<RELEASE>/TESTING/DEBUG`  

### System loading:

The library can be loaded into the operative system using one of the following, automatically generated, methods:    

* environment module file `~/.modules.d/edipack/<PLAT>/<VERSION>`  
* homebrew `bash` script `<PREFIX>/bin/edipack_configvars.sh`
* pkg-config file in `~/.pkg-config.d/edipack.pc`

### Python binding

Python binding (API) through module `edipy` can be  installed, once the library is successfully loaded in the OS, using the conventional toolchain:

`export F90=mpif90` (required if library has been compiled and installed with MPI support)  

 `pip install .`


### Uninstall

The library is removed with the command:

`make uninstall`

from the same building directory as for the installation part. 


### CREDITS
Using this code or any derivate of it please consider to cite the corresponding article [j.cpc.2021.108261](https://doi.org/10.1016/j.cpc.2021.108261) 



For any information contact the author as:  
adriano DOT amaricci @ gmail DOT com

--

***COPYRIGHT & LICENSING***  
Copyright  (c), Adriano Amaricci, Lorenzo Crippa, Alberto Scazzola, Francesco Petocchi, Giacomo Mazza, Luca de Medici, Massimo Capone.  
All rights reserved. 

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License (LGPL) as published by
the Free Software Foundation, either version 3 of the License, or any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU LGPL for more details.

You should have received a copy of the GNU LGPL along with this program.  If not, see <http://www.gnu.org/licenses/>.

Using this code please consider to cite the corresponding article [j.cpc.2021.108261](https://doi.org/10.1016/j.cpc.2021.108261) 

--



