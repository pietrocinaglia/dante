# DANTE
DANTE (DynAmic Networks alignment based on Temporal Embeddings) is a software tools for the aligment of dynamic networks based on temporal embeddings.

We tested DANTE on macOS Monterey (12.4), with CPU Intel.

<br />

## Requirements
DANTE needs Python >= 3.9 and Python Package Installer (pip), as well as the packages reported in 'requirements.txt'. The latter may be installed with the command:

```
pip3 install -r requirements.txt
```

or (alias pip=pip3):

```
pip install -r requirements.txt
```

<br />

## Run the example
You may use the dataset included into this repository, for demonstration purposes only, as follows:
```
.\DANTE example/dnet1/DN1 example/dnet2/DN2 example_alignment
```
The dataset consists of two dynamic networks (dnet1 and dnet2).
- dnet1: 10 nodes, 10 time points.
- dnet2: 20 nodes, 10 time points.

In 'example' the following files are available:
- 'example/dnet1': dnet1 (format in DANTE);
- 'example/dnet2': dnet2 (format in DANTE);
- 'example/dnet1.dy': dnet1 (format in DynaMAGNA++);
- 'example/dnet2.dy': dnet2 (format in DynaMAGNA++);
- 'example/results/DANTE': alignment (dnet1 on dnet2) produced by DANTE;
- 'example/results/DynaMAGNA++': alignment (dnet1 on dnet2) produced by DynaMAGNA++.

<br />

## Help
DANTE may be used as shell-command, or through its own Command Line Interface (CLI).

Arguments (arg):
1) Path of Dynamic Network_1 (G) *
2) Path of Dynamic Network_2 (H) *
3) Output's filename [Default: output]
4) (only CLI) Delimiter for data parsing [Default: space]

Run as shell-command: 
```
./DANTE arg1 arg2 arg3
```

Run CLI:
```
./DANTE
```

**Escaping spaces with backslash, in according to Linux/Unix Shell. For instance, /user1/my samples\s1 becomes /user1/my\ samples\s1*

Data is structured as edge list, one for each time point. To give an example, dnet1 consisting of 10 time points will have the following files inside a directory of the same name: DN11, DN12, DN13, DN1..., DN110.

<br />

## MIT License

Copyright (c) 2022

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.