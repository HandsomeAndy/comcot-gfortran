# comcot (gfortran)

 -  I've made comcot compatiable to gfortran since I started the GPU-comcot project. However, the original comcot, which runs on CPU serially, did not remain on my git history. Besides, I've heard of demands on gfortran compatiable comcot recently and it takes quite some efforts to transfer from ifort to gfortran for beginer who's not familiar with fortran. Therefore, I made this repo to respond the needs and make it as a benchmark to be able to test the speedup against GPU-comcot.

---

## **Requirements**

### **software**

>(possible supported version/developing environment):

- gfortran (4.1.2-46 ~ 8.2.0/4.8)

- GNU make (/3.82)

#### Notes: Platforms other than Linux
##### MacOS
 - gfortran compiler can be equipped with `gcc` at version 8. Therefore, the easiest way to install `gcc` is by `brew install` command , then you will have `gfortran` ready. Or reference the GNU [site](https://gcc.gnu.org) to build `gcc` by several of ways other than `brew`. [Here](https://gcc.gnu.org/wiki/GFortranBinariesMacOS) is the link instructing how to build precompiled `gcc` binary package for MacOS.
##### Windows
 - [Precompiled gcc](https://gcc.gnu.org/wiki/GFortranBinaries#Windows)


## **Installation**


### clone

```shell
git clone https://github.com/HandsomeAndy/comcot-gfortran.git
```

### Setup

#### GNU solftwares

- Generally, gnu `make` and `gfortran` are pre-installed on linux machines. Try `make --version` and `gfortran --version` to check if they exist. See 'Notes' for more informations.   


### Install

```shell
make
```

---

## Run a Simulation

- The input file of COMCOT is called `comcot.ctl`. Modify the file to specify a simulation time, time step, fault parameters, and grid settings. Additionally, a corresponding topographic file (available at [etopo](https://www.ngdc.noaa.gov/mgg/global/)) is required for grid construction, and the path to the file should be provided in `comcot.ctl`. For example, the fresh downloaded `comcot.ctl` takes `../etopo_halk2.xyz` as the topographic file and simulate the 2011 Tōhoku tsunami.

- To run the simulation, simply execute the program `comcot`

 ```shell
 ./comcot
 ```

## Features

![](https://i.imgur.com/cFhekyK.gif|width=2080)


## **Acknowledgements**

gfortran compatible version of COMCOT was developed by Tao, Chiu at Tsunami reseach group, IHOS, NCU. The goal of this work is to librate, coporate ideas with the community and accelerate the development of a high-throughput tsunami warning system at a relatively low cost. Original COMCOT version can be found at [here](http://223.4.213.26/archive/tsunami/cornell/comcot_down.htm).
