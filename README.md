# fortran-useful-functions
This repository will contain chunks of fortran code that will be useful while writing codes.

## Check if a file exists 
    INQUIRE (FILE = 'EE_LINKAGE.DAT', EXIST = FEXISTS)
      IF( FEXISTS )THEN
    
      ELSE

      ENDIF