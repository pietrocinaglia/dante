# DANTE
DANTE (DynAmic Networks alignment based on Temporal Embeddings) is a software tools for the aligment of dynamic networks based on temporal embeddings.

<br />

## Help
DANTE may be used as shell-command, or by using its Command Line Interface (CLI).

Arguments (arg):
1) Path of Dynamic Network_1 (G) *
2) Path of Dynamic Network_2 (H) *
3) Output's filename [Default: output]
4) Delimiter for data parsing (only through the CLI) [Default: space]

Run CLI:
```
./DANTE
```

Run as shell-command: 
```
./DANTE arg1 arg2 arg3
``` 

**If you use a path containing spaces, it must be reported in according to the shell syntax of unix; for instance, /user1/my samples\s1 becomes /user1/my\ samples\s1*

Data is structured as edge list, one for each time point. The latter is a network at t-time.

To give an example, a dynamic network (DN1) consisting of 5 time points will have the following files inside a directory of the same name: DN1/DN11, DN1/DN12, DN1/DN13, DN1/DN14, DN1/DN15.

<br />

## Run the example
You may use the dataset included into the repository, for demonstration purposes only, as follows:
```
.\DANTE example/dnet1/DN1 example/dnet2/DN2 example_alignment
```
The dataset consists of two dynamic networks (DN1 and DN2).
- DN1: 10 nodes, 10 time points.
- DN2: 20 nodes, 10 time points.

DANTE will produce a file ('example_alignment') consisting of the alignment.