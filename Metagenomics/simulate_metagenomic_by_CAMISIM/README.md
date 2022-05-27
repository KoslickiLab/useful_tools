# Simulate metagenomic reads by CAMISIM

CAMISIM is a powerful metagenomic simulator. Though BBMap is extremly simple and fast, you'll need CAMISIM for publication purpose (credit to Dr. Koslicki). CAMISIM can provide sample composition, alignment, and profile for simulation, making benchmark process friendly.

reference:
1. [CAMISIM github page](https://github.com/CAMI-challenge/CAMISIM)
2. [Use a new taxdump file](https://github.com/CAMI-challenge/CAMISIM/issues/81)
3. [Error free simulation](https://github.com/CAMI-challenge/CAMISIM/issues/53)

### Caveats in usage
---
1. Input genome files must be fa file, can't be gzipped
2. Run the cmd in the CAMISIM github folder (just follow the examples they give). In the design file for de novo running, the path for ENVs are relative path. Namely, you have to edit the path if you don't run the py code in the original folder. Similarly, you can't use full path inside the file because the python will paste the path together.
3. Input taxid is the species ID, otherwise you'll get an error.
4. Some new id may not in the older version of taxdump file, we can download the new and re-organise into a folder called "NCBI" (untar and then retar), see [issue 81](https://github.com/CAMI-challenge/CAMISIM/issues/81) for my description
5. CAMISIM can only be used under py27 environment

### How to run simulation
---
1. Create an conda environment with py27
2. Modify the [mini_config.ini](https://github.com/CAMI-challenge/CAMISIM/wiki/Configuration-File-Options) file (this is how CAMISIM take input parameters) by shadowing the structure of [input files](https://github.com/CAMI-challenge/CAMISIM/wiki/File-Formats)
3. Put your input files into the CAMISIM folder, and then run the py code inside the main folder


### Simulation types
---
CAMISIM is very powerful here, it can simulate short reads with or w/o seq errors, and simulate long reads from Nanopore. There are more to explore if you check their manual.
1. general short reads with seq error (default setting)
2. error free short reads (see my example)
3. long reads (try it youself lol)
