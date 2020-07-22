# Third Party Licenses
The following are open source modules used by GenevaERS

## Workbench
The following licensed code is used in the GenevaERS Workbench, the user interface.

Package (include version)   License (version if applicable)     URL for license statement
zlib 1.2.8                  Unique similar to BSD license       http://zlib.net/zlib_license.html
Xml4c 5.7                   Apache 2.0                          https://w3.xml.ibm.com/support/index.html
Xml Toolkit for z/OS, V1.10 Apache 2.0
ANTLR 2.7.7                 Unique similar to BSD license       http://www.antlr.org/license.html
Hashing code                Unique                              http://burtleburtle.net/bob/index.html
Eclipse RCP 4.4.2           EPL                                 https://www.eclipse.org/org/documents/epl-v10.php
Eclipse Nebula 1.1.0        EPL                                 https://www.eclipse.org/org/documents/epl-v10.php
BIRT 4.4.2                  EPL                                 https://www.eclipse.org/org/documents/epl-v10.php
COMFYJ 2.6		                                                  http://www.teamdev.com/comfyj/licensing/

We also use IBM Data Server Driver for ODBC and CLI  https://www.ibm.com/support/knowledgecenter/en/SSEPGG_10.5.0/com.ibm.db2.luw.apdv.cli.doc/doc/r0024162.html where it says you can download and install the IBM Data Server Driver for ODBC and CLI and use it with your ODBC and CLI applications without a special license.

## Performance Engine
There are no licensed subcomponents included in the Performance Engine.

## Build Processes
To build the SAFR product on z/OS requires:

1. High Level Assembler (HLASM) V1R6M0, normally present on a z/OS system, whilst not part of z/OS it is a non chargeable product.

2. SAFR currently uses IBM Enterprise Cobol for z/OS V4.2.

3. Similarly for C++ Compiles,  XL C/C++ is an optional priced feature

4. Run time includes Language Environment, in the z/OS base

5. Building the workbench uses InstallShield which a priced software product from Flexera.

6. DB2 database on z/OS
