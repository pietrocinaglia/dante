## DynAmic Networks alignment based on Temporal Embeddings (DANTE)

<i>DANTE</i> is a software tool for the alignment of dynamic networks based on temporal embedding.

It was developed based on the method published on the journal paper titled <i>"A Method Based on Temporal Embedding for the Pairwise Alignment of Dynamic Networks"</i> (reference is reported below).

We tested <i>DANTE</i> on macOS Monterey (12.4), with CPU Intel.

This is an extension of our preliminary prototype (version 1).

### Reference - Cite DANTE (version 2, or DANTEv2)

Cinaglia P, Cannataro M. A Method Based on Temporal Embedding for the Pairwise Alignment of Dynamic Networks. Entropy. 2023; 25(4):665. https://doi.org/10.3390/e25040665

#### Full-Text paper (Open-Access, Free PDF)
https://www.mdpi.com/1099-4300/25/4/665

#### Bibtex format:

@Article{dante2023,<br>
&nbsp;&nbsp;&nbsp;&nbsp;AUTHOR = {Cinaglia, Pietro and Cannataro, Mario},<br>
&nbsp;&nbsp;&nbsp;&nbsp;TITLE = {A Method Based on Temporal Embedding for the Pairwise Alignment of Dynamic Networks},<br>
&nbsp;&nbsp;&nbsp;&nbsp;JOURNAL = {Entropy},<br>
&nbsp;&nbsp;&nbsp;&nbsp;VOLUME = {25},<br>
&nbsp;&nbsp;&nbsp;&nbsp;YEAR = {2023},<br>
&nbsp;&nbsp;&nbsp;&nbsp;NUMBER = {4},<br>
&nbsp;&nbsp;&nbsp;&nbsp;ARTICLE-NUMBER = {665},<br>
&nbsp;&nbsp;&nbsp;&nbsp;URL = {https://www.mdpi.com/1099-4300/25/4/665},<br>
&nbsp;&nbsp;&nbsp;&nbsp;ISSN = {1099-4300},<br>
&nbsp;&nbsp;&nbsp;&nbsp;DOI = {10.3390/e25040665}<br>
}

<br />
<br />

### Requirements
<i>DANTE</i> needs Python >= 3.9, and the packages listed into 'requirements.txt'. The latter may be installed automatically by using [Python Package Installer (pip)](https://pip.pypa.io/en/stable/):

```
pip3 install -r requirements.txt
```

or (alias: pip=pip3):

```
pip install -r requirements.txt
```

<br />

### Run the example
You may use the dataset included into this repository ('example'), for demonstration purposes only, as follows:
```
./DANTE example/dnet1/DN1 example/dnet2/DN2 example_alignment
```
This dataset consists of two dynamic networks (dnet1 and dnet2).
- dnet1: 10 nodes, 10 time points.
- dnet2: 20 nodes, 10 time points.

The command will execute DANTE to produce the alignment ('example_alignment').

Summary:
- 'example/dnet1': dnet1 (format in DANTE);
- 'example/dnet2': dnet2 (format in DANTE);
- 'example/dnet1.dy': dnet1 (format in DynaMAGNA++);
- 'example/dnet2.dy': dnet2 (format in DynaMAGNA++);
- 'example/results/DANTE': alignment (dnet1 on dnet2) produced by DANTE;
- 'example/results/DynaMAGNA++': alignment (dnet1 on dnet2) produced by DynaMAGNA++.

<br />

### Help
<i>DANTE</i> may be used as shell-command, or through its own Command Line Interface (CLI).

Arguments (arg):
1) Path of Dynamic Network_1 (G) *
2) Path of Dynamic Network_2 (H) *
3) Output's filename [Default: output]
4) (only CLI) Delimiter for data parsing [Default: space]

Run as shell-command: 
```
./DANTE arg1 arg2 arg3
```

Run the CLI:
```
./DANTE
```

**Escaping spaces with backslash, in according to Linux/Unix Shell. For instance, /user1/my samples\s1 becomes /user1/my\ samples\s1*

Data is structured as edge list, one for each time point. To give an example, dnet1 consisting of 10 time points will have the following files inside a directory of the same name: DN11, DN12, DN13, DN1..., DN110.

<br />

### MIT License

Copyright (c) 2023

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
