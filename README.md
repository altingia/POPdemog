# POPdemog
Demographic history visualization from coalescent simulation script

Who to blame: Ying Zhou (yz001(at)uw(dot)edu)

## Installation

  install.packages("https://github.com/YingZhou001/POPdemog/raw/master/POPdemog_1.1.tar.gz", repos = NULL)

## Docs and materials: doc/

User can start with the [tutorial](doc/POPdemog-tutorial.md), and check function details with the [manual](doc/POPdemog-manual.pdf)
   
## Tools: tools/

### msprime2ms.py
Convert the demographic model specified in msprime to the ms-compatible format.

Usage:   
> python msprime2ms.py [demofile] [population_configurations] [migration_matrix] [demographic_events]   
  
>   [demofile] = input python file which specified the demographic model in msprime format   
>   [population_configurations] = name of the variable for population_configurations in msprime   
>   [migration_matrix] = name of the variable for migration_matrix in msprime   
>   [demographic_events] = name of the variable for demographic_events in msprime   

**Notes:**   
  + The python version should be the same as you use to install msprime.   
  + The reference effective population size is set as `Ne=10,000`, for the followed plot, `N4=4*Ne=40,000`.  
  + The sample size for each subpopulation is set as 1 since it is irrelevant here.   


An example:

python [tools/msprime2ms.py](tools/msprime2ms.py) [doc/demo1.py](doc/demo1.py) population_configurations migration_matrix demographic_events > msprime.demo.cmd
