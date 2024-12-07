# StructAlignPro

StructAlignPro provides a preloaded Cas-StructCores library for streamlined structural comparisons. StructAlignPro, embedding DALI9, a gold-standard structural comparison algorithm, while simplifying its usability. DALI's four-character filename limitation and intricate input requirements make it challenging to use. StructAlignPro manages this complexity through an intermediate file layer, allowing structural comparisons with only two input parameters. Both CRISPRCasStream and StructAlignPro offer broad versatility and can be applied to any CRISPR-Cas system mining or structural comparison tasks.
## License
This project is licensed under the MIT License. See the LICENSE file for more details.
## Package Dependencies
```
dnf install compat-libgfortran-48.x86_64       # requires root privileges
```
```
conda create -n structalignpro python=3.12  -y
conda install conda-forge::perl  -y
conda install wqiudao::structalignpro -y

```


## Usage
```
structalignpro 
```
<pre>
usage: structalignpro [-h] {pdb2dalidb,comparepdb,makedalidb} ...

Structure Alignment Program

positional arguments:
  {pdb2dalidb,comparepdb,makedalidb}
    pdb2dalidb          Compare a PDB file with DALI database.
    comparepdb          Compare two PDB files.
    makedalidb          Create DALI database: Converts a set of PDB files to DALI format numbers for subsequent structural searches.

options:
  -h, --help            show this help message and exit
</pre>

### pdb2dalidb
Use the built-in CAS core library to perform structural comparisons.
```
structalignpro pdb2dalidb test.pdb
```
### makedalidb
Use the subcommand `makedalidb` to create a custom reference structure database.

```
structalignpro makedalidb HEPN_REF_PDB_Cas13_abdhx
structalignpro pdb2dalidb --dali_database  HEPN_REF_PDB_Cas13_abdhx_dali test.pdb 
```
### comparepdb
Compare two PDB files.

```
structalignpro comparepdb test1.pdb test2.pdb 

```




Structure-enhanced streamlined approach reveals novel compact Cas13 proteins with non-canonical features



