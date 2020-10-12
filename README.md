# Instance Space Analysis for the Job Shop Scheduling Problem Data

## Features

The features are contained in the `features.csv` file.
The file is comma-separated and contains a single header row with the column names followed by a row for each instance.
For a detailled description of the individual features please refer to the thesis below.

## Benchmark results

For a detailled description of the methodology please refer to the thesis below.

### Data format
The results are contained in a separate csv file for each algorithm.
The csv files are comma-separated and contain a single header row with the column names followed by a row for each instance.
The columns are:
- `instance`: The name of the instance.
- `solve_time`: The time the algorithm took to produce a solution in seconds.
- `cmax`: The makespan of the generated solution.
- `solution`: A json string containing an array of arrays. Row `j` in the outer array corresponds to job `j` from the instance definition. Element `i` in the inner array then designates the start time of the `i`-th operation of job `j`.
Instances for which no solution, or an errornous solution, was found contain empty vlaues for `cmax` and `solution`.

### Evaluated Algorithms

#### Exact methods
- Chuffed (`chu`)
- CP Optimizer (`cpo`)
- OR-Tools (`ort`)

#### Heuristics
- Dispatching rule-based heuristic using the shortest processing sequence rule (`sps`)
- Dispatching rule-based heuristic using the longest processing sequence rule (`lps`)
- Dispatching rule-based heuristic using the shortest processing time rule (`spt`)
- Dispatching rule-based heuristic using the longest processing time rule (`lpt`)
- Dispatching rule-based heuristic using the least work remaining rule (`lwr`)
- Dispatching rule-based heuristic using the most work remaining rule (`mwr`)

#### Metaheuristics
- Random-restart hill climbing (`ran`)
- Tabu Search (`tab`)
- Simulated Annealing (`sim`)

## Instances

The instances and instance generator used can be found in the [strassl/jssp-instances](https://github.com/strassl/jssp-instances) repo.

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/)

## About

This work is part of Strassl, Simon. “Instance Space Analysis for the Job Shop Scheduling Problem.” Master’s Thesis, TU Vienna, 2020.
