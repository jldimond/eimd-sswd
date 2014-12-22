
### IPython Notebook and data supplemental to the manuscript: "_Up in arms: Immune and nervous system response to sea star wasting disease_"

<!---
INSERT LINKS HERE
--->

---

The repository includes a IPython notebook (.ipynb file) that can be downloaded locally and interactively executed. The code in the IPython notebook will download data and process data such that figures in the manuscript are reproduced (in theory). 

---
To execute the IPython Notebook in its entirety you will need:   

* IPython - [install instructions](http://ipython.org/install.html)    
* NBCI Blast -    
* R - [install instructions](http://www.r-project.org/)  
* rpy2 (interface to R from Python) - [install instructions](http://rpy.sourceforge.net/)  

---
###Description of Files

* `eimd_data.ipynb` - IPython notebok that can be interactively executed locally or viewed online.
* `data/Phel_transcriptome.fasta` - P hel coelocytes transcriptome. Contains xxxx contigs from de novo assembly.
* `data/Phel_countdata.txt` - Tab-delimited text file with read count data from 6 P hel RNA-seq libraries, 3 treated and 3 control libraries.
* `scripts/count_fasta.pl` - Perl script:  Author: Joseph Fass (modified from script by Brad Sickler) last revised: November 2010 - http://bioinformatics.ucdavis.edu.
* `wd` - subdirectory that serves as output directory (working directory) when the repository is downloaded and the IPython notebook is executed locally.

---
Note the current version of the IPython Notebook can be viewed (not interactive) in any web browser at: 
<http://nbviewer.ipython.org/github/che625/olson-ms-nb/blob/master/BiGo_dev.ipynb>

----
##Instructions

1) Download the repository zip file to a local directory and uncompress. This can be done by clicking on the link in the right sidebar or directly downloading: <https://github.com/che625/olson-ms-nb/archive/master.zip>

2) Launch IPython from the repository primary directory. 
For example, using Terminal on MacOSX.


```
$ cd /Desktop/olson-ms-nb
$ ipython notebook

```
This will launch IPython in your web browser.  
   
>_screenshot_    
![nb](http://eagle.fish.washington.edu/cnidarian/skitch/Home_1A41E21F.png)

3) Open notebook by clicking on **BiGo_dev.ipynb**. This will open a new tab in your browser.

>_screenshot_  
![nb2](http://eagle.fish.washington.edu/cnidarian/skitch/BiGo_dev_1A41E5C5.png)  



4) In theory, assuming all dependencies are installed

* BSMAP   
* bedtools   
* R   
* rpy2 (interface to R from Python)  

you could edit the cell near the top to provide the location of BSMAP on your machine, then run all cells (see screenshot). Raw data will be downloaded, and analyses carried out, producing figures (2) in manuscript. Please note data is very large (>20 GB) and analyses will take several hours depending on your machine.

>_screenshot_   
![nb3](http://eagle.fish.washington.edu/cnidarian/skitch/BiGo_dev_1A41EC5B.png)

In practice, you can execute cells individually with `shift-enter`.

---

We are actively trying to improve this realizing that we are likely missing dependancies, etc. Any suggestions and feedback is welcome. 

