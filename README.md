## Set up environment
We recommend you to set up a conda environment for packages used in this homework.

For part II, you need access to GPUs. 

You can either use HPC server (see documentation [here](https://github.com/Athul-R/NYU-HPC-Tutorials)) or use API services like lightning.ai. If using such service, you can skip conda commands and just install requirements in your studio.
```
conda create -n 1011-hw3 python=3.12.11
conda activate 1011-hw3
pip install -r requirements.txt
```

To register a jupyter kernel from your conda environment, use
```
conda activate 1011-hw3
python3 -m ipykernel install --user --name envkernel
```

## Running the tests

### Part 1
Run these from inside the `part1/` folder (running `python tests/test_tokenizer.py` directly fails with `No module named 'src'`):
```
cd part1
python -m tests.test_tokenizer              # Q1: BPE implementation tests
python -m tests.test_tokenizer properties   # Q2(a): tokenizer property tests
```
The Gradescope autograder runs these tests plus additional hidden ones.

### Part 2
Run from inside the `part2/` folder, after filling in `submission.py` (including your Hugging Face token and NetID) on a machine with a GPU:
```
cd part2
python run_tests.py
```
