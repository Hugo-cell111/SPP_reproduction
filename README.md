<p align="center">
  <h1 align="center"> Project for SPP </h1>
  
</p>

# Clone repository
```
git clone https://github.com/ChampSim/ChampSim.git
cd ./SPP_reproduction
```

# Compile

ChampSim takes five parameters: Branch predictor, L1D prefetcher, L2C prefetcher, LLC replacement policy, and the number of cores. 
For example, `./build_champsim.sh bimodal no no lru 1` builds a single-core processor with bimodal branch predictor, no L1/L2 data prefetchers, and the baseline LRU replacement policy for the LLC.
```
$ ./build_champsim.sh ${BRANCH} ${L1D_PREFETCHER} ${L2C_PREFETCHER} ${LLC_REPLACEMENT} ${NUM_CORE}
./build_champsim.sh perceptron no no lru 1
./build_champsim.sh perceptron no no lru 4
./build_champsim.sh perceptron no spp_dev_orig lru 1
./build_champsim.sh perceptron no spp_dev_orig lru 4
./build_champsim.sh perceptron no daampm lru 1
./build_champsim.sh perceptron no daampm lru 4
./build_champsim.sh perceptron no bop lru 1
./build_champsim.sh perceptron no bop lru 4
```

# Run simulation

Copy `scripts/run_champsim.sh` to the ChampSim root directory and change `TRACE_DIR` in `run_champsim.sh` <br>

then run the simulation. Remember to modify the dir of the traces before running.

```
nohup bash ./spp_commands.sh
```


