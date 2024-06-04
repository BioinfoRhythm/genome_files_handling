# Genome Copy Script
# Overview
This script is designed to copy selected genome files from a source directory to a target directory based on a list of specified genome IDs. It also creates a file listing any IDs that were not found in the source directory.
# Prerequisites
Python 3 installed on your system.
# Usage
Clone or download the repository containing the script.
Open the script file (genome_copy_script.py) in a text editor.
Set the following variables at the beginning of the script according to your directory structure:
source_directory: Path to the directory containing the genome files.
target_directory: Path to the directory where you want to copy the selected genome files.
missing_ids_file: Path to the file where missing IDs will be logged.
List: Path to the file containing the list of genome IDs.
Run the script. It will copy the genome files from the source directory to the target directory based on the IDs listed in the specified file.
# Script Details
The script uses the os module to interact with the file system.
It reads the list of genome IDs from the specified file (List).
For each file in the source directory, it checks if the ID matches any ID in the list.
If a match is found, it copies the file to the target directory.
If a match is not found, it logs a message indicating that the file was not moved.
# Example
Suppose you have a directory structure like this:
Project_1/
│
├── countrywise_data/
│   ├── asia/
│   │   ├── input/
│   │   │   ├── asia.txt
│   │   │   └── asia_missing.txt
│   │   └── output/
│   └── ...
│
└── genomes/
    ├── genome1.fna
    ├── genome2.fna
    └── ...
