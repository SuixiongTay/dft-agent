# dft-agent

An LLM Agent that can perform materials research and DFT calculations autonomously and share the results.

## Dataset Location

**Important for LLM agents**: All adsorption energy datasets are stored in `data/raw_data/` directory. The LLM should look for available datasets in this location when benchmarking our DFT calculations with the compiled datasets.

Available datasets include:
- `data/raw_data/CPD_H/` - CPD dataset with H species
- `data/raw_data/OC2020_H/` - OC2020 dataset with H species  
- `data/raw_data/jp4c06194_SI/` - Supporting information dataset

## Usage Example

For github issue 3:
```python
python -m backend.graph.qe_workflow \
 --structure_path data/slab.traj \
 --pseudo_dir ./pseudos/PBE \
 --workdir runs/pt111_co \
 --run_mode local \
 --thread_id pt111_co
```

## check read me to double check the schema, then write the code