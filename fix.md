# fix/

## General view
all text files (less than 1.5MB) will be tracked in the regional_workflow repo.
all binary or large text files will be tracked through 


all binary or large files are stored under FIX_RRFS
FIX_RRFS is located at a given location on Jet, Hera, Orion, WCOSS. rsync from Jet to other locations every day or on-change.

Jet: /lfs4/BMC/nrtrr/FIX_RRFS
Hera: 
Orion:
WCOSS:


all binary or large files under FIX_RRFS are put in read-only mode to avoid accidental delete or overwrite.
        chmod -w -R * .    and    chmod +w <file>
  

new version of binary/large files are encourged to add a descriptive suffix to self describe it, For example
      3drtma_berror_stats_heightDepedent_20200528
      fv3_akbk_65lvl_20210806
  
  
In operation implmentation, just use "cp" to make a hardened version

Any binary file larger than 5k and any files largeer than 1.5MB will be prevented to be commited.
         (use file command to determine file type, Sendmail frozen configuration)
  

domain directory only contains domain specific files (such as geo_em*, fv3_akbk, etc)

Don't use linked directory (crtma is an exception) as we cannot track individual files that way. Create corresponding directories and link files under it.
  
  
