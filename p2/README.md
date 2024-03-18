NOTE: - Scores have not been implemented (NR for intermediate) and has wrong values

How to compile code: 
    i.   On command line, navigate (cd) into the directory p2
    ii.  On the command line, run make <compile option> N=<Number of executables> (This creates the test folder with N executables and also generates an executable for the autograder) (compile option is exec and redir for intermediate)
    iii. Run autograder with the command ./autograder <solutions dir> arg1 arg2 arg3 ... (where B is the batch size, arg1, arg2, etc. are the command line arguments that each executale is run with) (The output will be printed in a file called "results.txt")

    eg.
    $ make redir N=5
    $ ./autograder solutions 1 2 3

Assumptions:
    i.   We have implemented alarm timers for long-running processes (Change 3)
    ii.  template.c has the line which prints the executable name, pid, mode and the case so the output has those lines before it prints something similar to the example above (this was given and I didn't change it)
    iii. For stuck/infloop case, I killed the process and updated the child_status to 2 in the timeout_handler(). In monitor_and_evaluate_solutions(), if child_status is 2, I give it case 4 and set child_status to -1 to indicate the process is not running anymore.
    iv.  We have janky way of handling stuck/infloop case (I don't know if it's the best way to do it, but we use alarm and but it works)
    v.   Maximum size of a string (filenames, filecontents, etc.) can be no more than 1024 bytes.

Team info: Group 18
    Members: Tamojit Bera (bera0041)
             Nikhil Kumar Cherukuri (cheru054)
             Pratham Khandelwal (khand113)
             Merrick McFarling (mcfar288)

Contributions: Tamojit (bera0041)
               Nikhil (cheru054) 
               Pratham (khand113)
               Merrick (mcfar288) 