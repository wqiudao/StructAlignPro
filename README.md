# StructAlignPro

This script is designed to optimize the usage of DaliLite.v5 for protein structure comparison.
It provides a simplified interface and enhanced functionalities, making it easier for users to perform structural alignments. This script has been developed with Python version 3
## License
This project is licensed under the MIT License. See the LICENSE file for more details.
## Date
2024-09
## Package Dependencies
dnf install compat-libgfortran-48.x86_64       # requires root privileges

conda create -n structalignpro python=3.12  -y
conda install conda-forge::perl 



## Usage
```
structalignpro 
```
<pre>
usage: StructAlignPro [-h] {makedalidb,pdb2dalidb,comparepdb} ...

Structure Alignment Program

positional arguments:
  {makedalidb,pdb2dalidb,comparepdb}
    makedalidb          Create DALI database: Converts a set of PDB files to DALI format numbers for subsequent
                        structural searches.
    pdb2dalidb          Compare a PDB file with DALI database.
    comparepdb          Compare two PDB files.

options:
  -h, --help            show this help message and exit
</pre>


```
structalignpro makedalidb HEPN_REF_PDB_Cas13_abdhx
```
<pre>
  Generating DALI database from HEPN_REF_PDB_Cas13_abdhx...
  
  /data8/StructAlignPro/HEPN_REF_PDB_Cas13_abdhx_dali
  
  Done
</pre>


```
structalignpro pdb2dalidb HEPN_REF_PDB_Cas13_abdhx_dali Cas13a_nc1.pdb 
```

<pre>
  Comparing Cas13a_nc1.pdb with database HEPN_REF_PDB_Cas13_abdhx_dali...
  /data8/StructAlignPro/Cas13a_nc1.pdb
  /data8/StructAlignPro/StructAlignPro_Cas13a_nc1_2024-11-17_23:51:19_result.txt
  Done
</pre>






```
structalignpro comparepdb Cas13a_nc1.pdb Cas13a_nc2.pdb 
```
<pre>
  Comparing Cas13a_nc1.pdb with another PDB file  Cas13a_nc2.pdb...
  /data8/StructAlignPro/StructAlignPro_Cas13a_nc1_vs_Cas13a_nc2_2024-11-17_23:54:06_result.txt
  Done  
</pre>






