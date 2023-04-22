# caboose

This repository contains the code for our recent SIGIR paper on unlearning data from kNN recommendations models:

_Sebastian Schelter, Mozhdeh Ariannezhad, Maarten de Rijke (2023). Forget Me Now - Fast and Exact Unlearning in Neighborhood-Based Recommendation. ACM SIGIR'23_ 

This code contains the Python frontend and the integration into next-basket recommendation algorithms. The Rust code for the underlying index is available at https://github.com/schelterlabs/caboose_index .


## Installation for Development

### Preliminaries
 * Make sure you have Python 3.9 and Rust installed: https://www.rust-lang.org/tools/install
 * Make sure to have https://github.com/schelterlabs/caboose_index checked out as `caboose_index` in the same folder as this project
 
### Dependencies and build 
 * Setup a virtualenv `python3.9 -m venv venv` and `source venv/bin/activate`
 * Install Cython (needed for similaripy) `pip install Cython==0.29.32`
 * Install the dependencies `pip install -r requirements.txt`
 * Build the project with `maturin develop --release`
 
### Validation
 * Run the tests with `pytest`
 * Start `jupyter` and run the `minimal` notebook
