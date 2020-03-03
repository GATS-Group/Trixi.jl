# Trixi: A tree-based flexible DG/SBP framework written in Julia

## Installation
Strictly speaking, no installation is necessary to run Trixi. However, the
simulation program and the postprocessing tools rely on a number of Julia
packages, which need to be available on the respective machine. This can most
easily be achieved by performing the following steps:

1.  Clone the repository:
    ```bash
    git clone git@gitlab.mi.uni-koeln.de:numsim/code/Trixi.jl.git
    ```
2.  Enter the cloned directory and run the Julia command-line tool:
    ```bash
    cd Trixi.jl
    julia
    ```
3.  Switch to the package manager with pressing `]`, activate the current
    directory and then instatiate it:
    ```julia
    julia> ]
    (v1.3) pkg> activate .
    Activating environment at `~/path/to/Trixi.jl/Project.toml`

    (Trixi) pkg> instantiate
    ```


## Usage
Enter the root directory `Trixi.jl` and run
```bash
bin/trixi
```

To change the simulation setup, edit `parameters.toml`.


## Style guide
The following lists a few conventions that have been used so far:

*   Modules, types, structs with `CamelCase`
*   Functions, variables with lowercase `snake_case`  
*   Indentation with 2 spaces (never tabs!), line continuations indented with 4
    spaces
*   Maximum line length (strictly): **100**
*   Prefer `for i in ...` to `for i = ...` for better semantic clarity and
    greater flexibility

Based on that, and personal experience, a formatting tool with a few helpful
options is included in `utils/julia-format.jl`. Note, however, that this tool is
not yet optimal, as it re-indents too greedily.

This is a list of handy style guides that are mostly consistent with each
other and this guide, and which have been used as a basis:

*   https://www.juliaopt.org/JuMP.jl/stable/style/
*   https://github.com/jrevels/YASGuide

## Authors
Trixi was created by Michael Schlottke-Lakemper and Gregor Gassner.