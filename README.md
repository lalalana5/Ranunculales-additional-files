Files uploaded here were described and used in creation of protocol that explains Studying plant specialized metabolites using molecular networking.

Available files include: 
1. .txt file with names of raw files used in the analysis. This file is important for automated download of raw files from the MassIVE repository (MSV000087728).
2. .tsv file with metadata for the analyzed dataset.
3. .xml file needed for Batch processing.
3. .csv outputs from SIRIUS analysis.
4. .csv outputs from MS2Query analysis.


## **Downloading the raw files from MassIVE**

In order to download a subset of files from MassIVE using command line, we have to create a text file with the names of files we want to download. The file used to download Ranunculales dataset can be downloaded from this repository and it is under the name "Ranunculales-IDs.txt".

Next, open the command prompt on your computer, navigate to the folder where the text file with ID’s was saved using:

```
cd <path-to-the-folder>
```

Once you are in the same folder, run the following command after replacing file-with-IDs.txt with your text file's name.

```
for filename in $(cat file-with-IDs.txt); do wget ftp://massive.ucsd.edu/MSV000087728/raw/VGF_pos_with_QC_and_blanks_raw/$filename; done
```

Pressing the <Enter/Return> key will start the download of .raw files from MassIVE.
