How to define a workflow for your new analyses (*work in progress*)
==============================================

1. Write a new *samples.tab* file where you describe your samples
2. Write a new *design.tab* file where you describe your sample grouping and comparing to each other (Control, Treatment, etc)
3. Write a new *config.yml* file where you define all parameters to your workflow 
4. Write a new workflow file *new_analysis.wf* in snakemake defining the workflow to perform. 

Check the [examples directory](https://github.com/TAGC-bioinformatics/gene-regulation/tree/master/examples) of the project for existing examples of workflows that could serve as templates.

## samples.tab file ##

* In case of Single ended analyses : First column named ID **should** be the name of your file without the file extension as it appears in your data : ex ID of sample file bla_bli_blu.fastq is bla_bli_blu.
* In case of Paired ended analysis the ID **should not** contain the strand 1 or 2, example ID of file bla_bli_blu_1.fastq should be bla_bli_blu. This has to do with [issue number \#2] (https://github.com/TAGC-bioinformatics/gene-regulation/issues/2) on the issue tracker of the project. In that case one **has to** put the strand information in the config.yml file. 
* The "Condition" named column **can** contain the different conditions to compare
  
## design.tab file ##
Tabulated file. 
* **Should** contain two columns. *TODO* : check this
* The first column *is* the Reference condition towards the other conditions (next column) will be compared. *TODO* : is this order important/relevant?
