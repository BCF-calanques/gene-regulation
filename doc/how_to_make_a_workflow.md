How to define a workflow for your new analyses
==============================================

1. Write a new samples.tab file where you describe your samples
2. Write a new design.tab file where you describe your sample grouping and comparing to each other (Control, Treatment, etc)
3. Write a new config.yml file where you define all parameters to your workflow 
4. Wite a new workflow file new_analysis.wf defining the workflow to perform

## samples.tab file ##

What is mandatory contains "should" or "cannot", what is optional contains "can":
* In case of Single ended analyses : First column named ID has to be the name of your file without the file extension as it appears in your data : ex ID of sample file bla_bli_blu.fastq is bla_bli_blu.
* In case of Paired ended analysis the ID should not contain the strand 1 or 2, example ID of file bla_bli_blu_1.fastq should be bla_bli_blu. In that case one has to put the strand information in the config.yml file. This has to do with issue number \#2 on the [issue tracker](https://github.com/TAGC-bioinformatics/gene-regulation/issues/2) of the project.
* The "Condition" named column can contain the different conditions to compare
* 
  
## design.tab file ##
Tabulated file. 
* Has to contain two columns.
* The first column is the Reference condition towards the other conditions (next column) will be compared. *TODO* : is this order important/relevant?
