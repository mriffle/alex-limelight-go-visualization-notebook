# alex-limelight-go-visualization-notebook

Jupyter Notebook for drawing GO DAGs of Limelight peptide results.

For each peptide, this tool will:

  1. Find all GO annotations for all proteins that peptide is in.
  2. Get all ancestors terms for those annotations all the way to the root.
  3. Merge all of these annotations into a single set.
  4. Increment the PSM count for all of the terms in the set by the PSM count for this peptide.

Afterwards, the resulting GO DAG is drawn using supplied colors and PSM and protein counts.

## Requirements

### Graphviz
Graphviz is a graphing library that must be installed.

On Windows, open an Anaconda prompt and type: `conda install -c alubbock pygraphviz`
Note: this also installs `pygraphviz`, another requirement.

### Python requirements

- Mike Riffle's GO library called PyGON: https://github.com/mriffle/pygon
  Clone to a directory and change the `sys.path.append(r'c:\Users\mriffle\IdeaProjects\pygon')` to this path.
- `pygraphviz` (Note, this may be installed by above `conda` command)
- `IPython`
- `pandas`

