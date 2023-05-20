Installations

# Pre-requisites

* Ensure you have `Miniconda` installed and can be run from your shell. If not, download the installer for your platform here: https://docs.conda.io/en/latest/miniconda.html

     **NOTE**

     * If you already have `Anaconda` installed, go ahead with the further steps, no need to install miniconda.
     * If `conda` cmd is not in your path, you can configure your shell by running `conda init`.

* Ensure you have `git` installed and can be run from your shell

     **NOTE**

     * If you have installed `Git Bash` or `Git Desktop` then the `git` cli is not accessible by default from cmdline.
       If so, you can add the path to `git.exe` to your system path. Here are the paths on a recent setup

```
        %LOCALAPPDATA%\Programs\Git\git-bash.exe
        %LOCALAPPDATA%\GitHubDesktop\app-<ver>\resources\app\git\mingw64\bin\git.exe
```

* Ensure [invoke](http://www.pyinvoke.org/index.html) tool and pyyaml are installed in your `base` `conda` environment. If not, run

```
(base):~$ pip install invoke
(base):~$ pip install pyyaml
```

# Getting started

* Switch to the root folder (i.e. folder containing this file)
* A collection of workflow automation tasks can be seen as follows
    **NOTE**

     * Please make sure there are no spaces in the folder path. Environment setup fails if spaces are present.

```
(base):~/<proj-folder>$ inv -l
```

* To verify pre-requisites, run

```
(base)~/<proj-folder>$ inv debug.check-reqs
```

and check no error messages (`Error: ...`) are printed.


`

### Setup a development environment:

Run below to install core libraries
```
(base):~/<proj-folder>$ inv dev.setup-env --usecase=<specific usecase>
```

