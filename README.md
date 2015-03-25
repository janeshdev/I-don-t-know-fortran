# I don't know ForTRAN
This repository will contain chunks of fortran code that will be useful while writing codes.

Here are some useful functions / pieces of code that you would find helpful while using these commands on your projects. Please report any issues / comments on `issues` section of this repository. 

## Functions
[Check if file exists]()


### Check if a file exists 
    INQUIRE (FILE = 'EE_LINKAGE.DAT', EXIST = FEXISTS)
      IF( FEXISTS )THEN
    
      ELSE

      ENDIF

### Conditional debugging in Fortran 

While debugging the code, we might be interested to debug line by line when certain conditions is met. To do that in visual studio, we need to first create a break point and right click on the break point. The following options will pop up: 

![Breakpoint Options](https://github.com/janeshdev/I-don-t-know-fortran/blob/master/images/breakpoint-options.png)

Then we can click on `Condition` and then insert the condition as if we were writing an `if` statement. 

![Breakpoint Condition](https://github.com/janeshdev/I-don-t-know-fortran/blob/master/images/breakpoint-condition.png)