# StructAlignPro

This script is designed to optimize the usage of DaliLite.v5 for protein structure comparison.
It provides a simplified interface and enhanced functionalities, making it easier for users to perform structural alignments. This script has been developed with Python version 3
## License
This project is licensed under the MIT License. See the LICENSE file for more details.
## Author
wang qiudao (wqiudao@gmail.com)
## Date
2024-09
## Usage
Usage: StructAlignPro [-h] {makedalidb,pdb2dalidb,comparepdb} ...
Structure Alignment Program
positional arguments:
  {makedalidb,pdb2dalidb,comparepdb}
    makedalidb          Create DALI database: Converts a set of PDB files to DALI format numbers for subsequent structural searches.
    pdb2dalidb          Compare a PDB file with DALI database.
    comparepdb          Compare two PDB files.
options:
  -h, --help
