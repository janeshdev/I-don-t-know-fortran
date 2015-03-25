# I don't know ForTRAN
This repository will contain chunks of fortran code that will be useful while writing codes.

Here are some useful functions / pieces of code that you would find helpful while using these commands on your projects. Please report any issues / comments on `issues` section of this repository. 

## Functions
[Check if file exists]()


### Check if a file exists 

	! DEFINE FEXISTS as LOGICAL
	LOGICAL FEXISTS 
    INQUIRE (FILE = 'Filename.DAT', EXIST = FEXISTS)
      IF( FEXISTS )THEN
    
      ELSE

      ENDIF

### Conditional debugging in FORTRAN 

While debugging the code, we might be interested to debug line by line when certain conditions is met. To do that in visual studio, we need to first create a break point and right click on the break point. The following options will pop up: 

![Breakpoint Options](https://github.com/janeshdev/I-don-t-know-fortran/blob/master/images/breakpoint-options.png)

Then we can click on `Condition` and then insert the condition as if we were writing an `if` statement. 

![Breakpoint Condition](https://github.com/janeshdev/I-don-t-know-fortran/blob/master/images/breakpoint-condition.png)

### Open and close files in FORTRAN 

To open files in FORTRAN simply use: 

	OPEN(7, FILE = 'hello.txt', STATUS = 'UNKNOWN')
where 7 = the unique number assigned to the file that is being opened. 

To close the files we can simply use :

	CLOSE(7)
If we want to delete the file then we can use 
	CLOSE(7, STATUS = 'DELETE')

### Append files in FORTRAN 

To do the appends in FORTRAN we could do something like: 

	OPEN(95,FILE=OUTDIR//'*.OUT',POSITION='APPEND',STATUS='OLD',  FORM='BINARY')
	! Some code 
	CLOSE(95) 

In the above code `95` is just used arbitrarily. 

### Allocatable arrays in FORTRAN 90

In FORTRAN 90, one can assign allocatable arrays with the syntax as follows:

	REAL,ALLOCATABLE,DIMENSION(:)::RSSBCW
	REAL, ALLOCATABLE, DIMENSION(:,:):: TESTDF

In the above example,  `RSSBCW` is a 1-D vector whereas `TESTDF` is a 2 dimensional array. 

### Using modules 

A simple module structure would look something like: 

	MODULE COMPUTATION
	
	! Assign some variables 
	SAVE
	
	! Add pieces of code / Functions 
	
	END MODULE COMPUTATION

Now, while referring to the main program, you can use a simple syntax as follows: 

	USE COMPUTATION
After that we would be able to access all the code written in the modules. So, I think it is very useful way to write bunch of functions and subroutines into one program. 

