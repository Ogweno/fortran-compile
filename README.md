### Compile Fortran program files

**compile** is a shell script which compiles Fortran files using `gfortran`. It can be invoked in the command-line as
`pauls:~$ compile mainfortranfile.f90`
where, `mainfortranfile.f90` is the main fortran program file.

A specific convention is followed for naming the program and module files. The main program file is named using the convention `main*.f90`. This main program connects to various modules using the syntax `use modulename`. The program file containing this module has to be named `modulename.f90`. The **compile** script looks inside the `main*.f90` file to determine the name of the module files. It then compiles all the required files using `gfortran`. The main and module file needs to be in the same directory. The script also works if the main program file is arbitrarily named, however, the naming convention for the module files has to be followed.

### Installation

Download the file, and then do `sudo mv compile /usr/local/bin`.
