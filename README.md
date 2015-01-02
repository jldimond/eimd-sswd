
### IPython Notebooks and data supplemental to the manuscript: "_Up in arms: Immune and nervous system response to sea star wasting disease_"

<!---
INSERT LINKS HERE
--->

---

The repository includes IPython notebooks (.ipynb file) that can be downloaded locally and interactively executed. The code in the IPython notebook **eimd_analysis.ipynb** will process data such that figures in the manuscript are reproduced (in theory). 

---
###Description of Files

* `eimd_analysis.ipynb` - IPython notebok that can be interactively executed locally or viewed online designed so that user can **replicate all analysis**. Requires several ependancies (see above)
*  `eimd_data-only.ipynb` - IPython notebok that can be interactively executed locally or viewed online designed so that user can **simply explore** data files. _Only requires IPython_.
* `data/Phel_transcriptome.fasta` - P hel coelocytes transcriptome. Contains xxxx contigs from de novo assembly.
* `data/Phel_countdata.txt` - Tab-delimited text file with read count data from 6 P hel RNA-seq libraries, 3 treated and 3 control libraries.
* `scripts/count_fasta.pl` - Perl script:  Author: Joseph Fass (modified from script by Brad Sickler) last revised: November 2010 - http://bioinformatics.ucdavis.edu.
* `wd` - subdirectory that serves as output directory (working directory) when the repository is downloaded and the IPython notebook **eimd_analysis.ipynb** is executed locally.
*  `precompiled_wd` - subdirectory thatprovides all data that will be produced in `wd` by running commands in notebook. Used primarily for viewing data in **eimd_data-only.ipynb**

---


#Instructions for data-only (interactive viewing) notebook


1) Download the repository zip file to a local directory and uncompress. This can be done by clicking on the link in the right sidebar or directly downloading: <https://github.com/sr320/eimd-sswd/archive/master.zip>

2) Launch IPython from the repository primary directory. 
For example, using Terminal on MacOSX.


```
$ cd /Desktop/eimd-sswd
$ ipython notebook

```
This will launch IPython in your web browser.  


3) Open notebook by clicking on **eimd_data-only.ipynb**. This will open a new tab in your browser.


4) Execute code as written or modify to your likely. To execute cell type *shift-enter*.

---


#Instructions for analysis (interactive execution) notebook

1) **Before you get started**

To execute the **eimd_analysis.ipynb** IPython Notebook in its entirety you will need:   

* IPython - [install instructions](http://ipython.org/install.html)    
* NBCI Blast -  [install instructions](http://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download)  
* R - [install instructions](http://www.r-project.org/)  
* rpy2 (interface to R from Python) - [install instructions](http://rpy.sourceforge.net/)  
* SQLShare-pythonclient [install instructions](https://github.com/uwescience/sqlshare-pythonclient)

---

In addition you will need a local copy of the UniProt/SwissProt Blast Database. 
If you do not already have this database you can create it once you install NCBI Blast. Create a blast database first download a fasta file from <http://www.uniprot.org/downloads> that of Reviewed (Swiss-Prot) then run make blastdb commands.
Below is an example code if you wanted to create the database in a subdirectory named `blastdb`. This will result in files > 300 MB.

`$ mkdir blastdb`

`$ cd blastdb`

`$ curl -O ftp://ftp.uniprot.org/pub/databases/uniprot/current_release/knowledgebase/complete/uniprot_sprot.fasta.gz`

`$ gunzip uniprot_sprot.fasta.gz`

`$ makeblastdb -in uniprot_sprot.fasta -dbtype prot -out uniprot_sprot`

This will generate a Protein database that you can you to blast sequences. 

---

2) Download the repository zip file to a local directory and uncompress. This can be done by clicking on the link in the right sidebar or directly downloading: <https://github.com/sr320/eimd-sswd/archive/master.zip>

2) Launch IPython from the repository primary directory. 
For example, using Terminal on MacOSX.


```
$ cd /Desktop/eimd-sswd
$ ipython notebook

```
This will launch IPython in your web browser.  


3) Open notebook by clicking on **eimd_analysis.ipynb**. This will open a new tab in your browser.



4) Modify the cell near the top of the notebook …

```
#Variables user needs to modify accordingly
db="~/blastdb/uniprot_sprot"
sqls="~/sqlshare-pythonclient/tools/"
usr="sr320@washington.edu"
```
`db` refers to location of blastdb (instructions on bow to create database in _step 1_).   
`sqls` refers to the location of your sqlshare-pythonclient tools subdirectory (instructions to install in _step 1_).   
`usr` refers to your SQLshare user name (yep, see _step 1_ if need be)


5) Execute code as written or modify to your liking. To execute cell type *shift-enter*. Once variables are set, you should be able to run all cells.


---

We are actively trying to improve this realizing that we are likely missing dependancies, etc. Any suggestions and feedback is welcome. 

