=== Zip File Contents === 

1. <catalog name>.xml - reference of the Dell Update Packages (DUPs) that you enabled for this update.

2. Dell.Command.Repository.Maker.exe - an .exe file that reads the <catalog name>.xml file then downloads and caches the DUPs.

3. This README.txt file 



=== Instructions ===

1. From a command prompt, run Dell.Command.Repository.Maker.exe using appropriate command line arguments, as noted below. 

2. This automates the following:

   - Reads <catalog name>.xml

   - Downloads and caches the relevant DUPs to a target location you specify, creating the appropriate directory structure

   - Updates the source location in <catalog name>.xml to a target location you specify, which dictates the location from which the the Dell Command | Update tool downloads DUPS during an update. 



=== Command Line Arguments ===

  -?|-h|--help              Show help information

  -c|--catalog <file>       Defines the catalog file you wish to use. Ex: -c "catalog.xml"

  -t|--target <path>        Defines the target path for the downloads. Ex: -t "c:\myDirectory\"

  -b|--baseLocation <path>  Defines the new baseLocation in the catalog file. Ex: -b "\\foo\stuff\catalogs"
  
  -f|--force		        Defines a forced-download. Ex: -f



Note: If no catalog file is specified, "catalog.xml" will be searched for in the current folder. 

Note: When the -b| option is used, the original <catalog name>.xml file will be copied to <catalog name>.xml.orig. You can use -b with the Dell Command | Update tool.


=== Dell Command Repository Maker Tool ===

(C) Copyright 2020, Dell Inc., All Rights Reserved.