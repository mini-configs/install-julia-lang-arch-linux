### Julia lang installation & Add Julia to Jupyter Notebook

Here we install Julia in ~/opt/julia-1.0.1:
``` console 

mkdir ~/opt
cd ~/opt
wget https://julialang-s3.julialang.org/bin/linux/x64/1.0/julia-1.0.1-linux-x86_64.tar.gz
tar -xvf julia-0.5.0-linux-x86_64.tar.gz
rm julia-0.5.0-linux-x86_64.tar.gz
```

Launch julia by issuing ~/opt/julia-0.5.0/bin/julia and install the following additional packages:
``` julia
[user@batman opt]$ ~/opt/julia-1.0.1/bin/julia 
               _
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.0.1 (2018-09-29)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

julia> using Pkg

julia> Pkg.add("IJulia")


julia> using Pkg

Cloning default registries into /home/mirian/.julia/registries
   Cloning registry General from "https://github.com/JuliaRegistries/General.git"
  Updating registry at `~/.julia/registries/General`
  Updating git-repo `https://github.com/JuliaRegistries/General.git`
 Resolving package versions...
    ... 
```
Adapt the environment variable `PATH`:

`export PATH="$HOME/opt/julia-1.0.1/bin:$HOME/.local/bin:$PATH"`
