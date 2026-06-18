# Third Party Licenses
The following are open source modules used by GenevaERS

## Workbench
The following licensed code is used in the GenevaERS Workbench, the user interface.

Package (include version)   
-->License (version if applicable)    
---->URL for license statement

Xml4c 5.7                   
-->Apache 2.0                          
---->https://w3.xml.ibm.com/support/index.html

Xml Toolkit for z/OS, V1.10
-->Apache 2.0

Eclipse RCP 4.4.2           
-->EPL                                 
---->https://www.eclipse.org/org/documents/epl-v10.php

Eclipse Nebula 1.1.0        
-->EPL                                 
---->https://www.eclipse.org/org/documents/epl-v10.php


## Performance Engine
IBM High Level Assembler and Toolkit V1R6M0
--> #Commercial
---->https://www.ibm.com/us-en/marketplace/high-level-assembler-and-toolkit-feature

# z/OS Build Process Tooliing

The z/OS Performance Engine requires IBM z/OS operating system.
- CPU: Requires a minimum of 1 CPU.  For parallel processing access to more than one CPU is required. 
- Memory: 1 GB minimum. 
- Disk: 1 GB for the system, independent of the data you will process with it.

## Minimum Required Tools
To build the SAFR product on z/OS requires:

1. High Level Assembler (HLASM) V1R6M0, normally present on a z/OS system, whilst not part of z/OS it is a non chargeable product.

2. High Level Assembler Toolkit V1R6M0, a separate costed product for z/OS

## Suggested Tools

3. z/OS Java

## Optional Tools

1. DB2 database on z/OS can be used for a shared metadata environment.

2. User Exit development can be done in IBM Enterprise Language Environemnt, using for example Cobol for z/OS V4.2 if desired.


