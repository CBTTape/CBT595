# CBT595
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 595 is from Richard L. Rice and contains a macro which    *   FILE 595
//*           is used to trace the execution of a program.          *   FILE 595
//*                                                                 *   FILE 595
//*           email:  rlrice@skylark.ppco.com                       *   FILE 595
//*                                                                 *   FILE 595
//*    Description of the LABEL macro:                              *   FILE 595
//*                                                                 *   FILE 595
//*      This macro provides a method to trace program execution    *   FILE 595
//*      in assembler language programs.  The macro replaces the    *   FILE 595
//*      'EQU *' or 'DS 0H' commonly used to define labels.  The    *   FILE 595
//*      names used in the "label" field are stored in an in        *   FILE 595
//*      core "wrap-around" table.                                  *   FILE 595
//*                                                                 *   FILE 595
//*      The 'TRACE' keyword allows you to turn tracing on and      *   FILE 595
//*      off at various points.  This parameter sets a global       *   FILE 595
//*      switch so if trace is turned off at some point, the        *   FILE 595
//*      following LABEL macros will not cause tracing until you    *   FILE 595
//*      turn TRACE back on.  This may prevent the trace table      *   FILE 595
//*      from becoming flooded with trace entries you do not        *   FILE 595
//*      need for problem determination.  Also, after the           *   FILE 595
//*      program is debugged, code 'TRACE=OFF' or 'TRACE=NO' on     *   FILE 595
//*      the first LABEL macro and there will be zero overhead      *   FILE 595
//*      in storage use or execution time (all the macro will       *   FILE 595
//*      generate will be the actual assembler label).              *   FILE 595
//*                                                                 *   FILE 595
//*      Overhead is 12 bytes per LABEL, plus the size of the       *   FILE 595
//*      trace routine (generated via "LABEL TRACE=ROUTINE"),       *   FILE 595
//*      plus the size of the trace table (dynamically acquired,    *   FILE 595
//*      but not freed).  You probably don't want to just leave     *   FILE 595
//*      the trace stuff on once you get the program working        *   FILE 595
//*      because the trace table is not freed.  There is some       *   FILE 595
//*      execution time overhead also, of course.                   *   FILE 595
//*                                                                 *   FILE 595
//*      The macro uses and changes register 15.  On the first      *   FILE 595
//*      call, the code will issue a GETMAIN.  GETMAIN uses         *   FILE 595
//*      registers 0, 1, 14, and 15.                                *   FILE 595
//*                                                                 *   FILE 595
//*      The trace routine uses in-line work areas, so programs     *   FILE 595
//*      using the LABEL macro are not re-entrant.                  *   FILE 595
//*                                                                 *   FILE 595
//*      There are three eyecatchers in the trace routine to        *   FILE 595
//*      help you find the trace table.  These are "TRACE1ST",      *   FILE 595
//*      "TRACECUR", and "TRACELST".  TRACECUR will be the last     *   FILE 595
//*      entry added.  Good news is if your program abends, all     *   FILE 595
//*      you have to do is find the eyecatchers and get the         *   FILE 595
//*      addresses.  Bad news is if your program runs, but just     *   FILE 595
//*      doesn't work correctly, you will have to cause an abend    *   FILE 595
//*      in order to get a dump.                                    *   FILE 595
//*                                                                 *   FILE 595
```
