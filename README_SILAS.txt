this is the current programs as of 1045 pm on 05062016 installed in APT company, APTECH

the 3625_* files are installed in Global Files directory. 

the IMPORT,EXPORT,RUNNING files are RUN files for programs to know whether or not the PID is still running for the previous
gab instance so they do not try to run again. 

3625_IMPORT_ERRORS - logs import errors instead of the program locking up with a message box. 

3625_EXPORT_ERRORS - logs import errors instead of the program locking up with a message box.

Bothe othe error logs are done within error handling in both programs, when the end the program , it deletes the run file
so that the watchdog program will know whether or not program was ended. 
the watchdog program also verifies the PID in the RUN file and if it does not match it will launch the import/export program auto so that it does not stop.

Error logs for both can be viewed from the watchdog program. 
