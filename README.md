# fortran-useful-functions
This repository will contain chunks of fortran code that will be useful while writing codes.

## Functions
[Check if file exists](#check)


## Check if a file exists<a name = "check"></a> 
    INQUIRE (FILE = 'EE_LINKAGE.DAT', EXIST = FEXISTS)
      IF( FEXISTS )THEN
    
      ELSE

      ENDIF