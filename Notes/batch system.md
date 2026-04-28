- batch docs: https://batchdocs.web.cern.ch/index.html
# Basic concept
![[Pasted image 20260424194200.png]]

# Job Flavors
```
espresso     = 20 minutes 
microcentury = 1 hour 
longlunch    = 2 hours 
workday      = 8 hours 
tomorrow     = 1 day 
testmatch    = 3 days 
nextweek     = 1 week
```
The default job flavour for a job submitted with no other information is "espresso".

Setting the job flavour in the submit file is achieved like this:
```
+JobFlavour = "longlunch"
```

Setting manually can be achieved by placing the following in your submit file:
```
+MaxRuntime = Number of seconds
```

# EosSubmit schedds
- linked [here](https://batchdocs.web.cern.ch/local/eossubmit.html)
The main point of EosSubmit schedds is that, contrary to standard schedds, all defined files related to the job must be located in EOS. This includes the executable, the user log, the stdout/err/input files, and the files to transfer as input. Also, the destination path of output files to transfer must be in EOS.

The easiest way to achieve this is to `cd` to some EOS path (`/eos/...`) within your submission machine and use relative paths in the submit file. Alternatives are to set `initialdir` to an EOS directory, or use absolute `/eos/...` paths. Several [examples below](https://batchdocs.web.cern.ch/local/eossubmit.html#Examples) illustrate these possibilities.

Once the submit file is ready, using EosSubmit schedds is fairly simple:
- First, select the schedds:    
```
module load lxbatch/eossubmit
```
Note that to switch back to normal schedds you would need to run 
```
module unload lxbatch/eossubmit
```
or
```
module load lxbatch/share
```
- Then, just use the normal submit command:
```
condor_submit <submit file > [...]
```
Everything should work out fine for your job, and xrootd used transparently for all file transfers avoiding fuse or shared filesystems altogether.

# The initialdir Parameter
In the case where the files (input and output) are stored in an other directory than where the submission takes place, the initialdir command can be used in the submit description file. It is important to understand that initial directory is related to the input and output files and **not** related to the executable. This means that if the executable is in this directory, it is necessary to specify the fully qualified name of the _executable_. If just the name of the executable is set, it will not be found.