# Building

To build, go into the scripts directory and run the `compile_script.sh` script

```
cd scripts
./compile_script.sh 
```

<!-- ```
cmake <path_to_source_directory>
make
```
in your shell. -->

This will create programs named
* `build/bin/prime_finder`
* `build/bin/part1_tests`
* `build/bin/part1_bench`
* `build/bin/gs_serial`
* `build/bin/gs_parallel`
* `build/bin/part2_tests`
* `build/bin/part2_bench`
* `build/bin/combined_tests`
* `build/bin/combined_bench`

It will also put example data files into a directory named
`./data`

# Running the programs

You can run the programs by typing

`./scripts/submit_batch.sh` from the mp2 root directory

Or, if you'd like to run the program without testing and benchmarking, you can do

`build/bin/gs_serial <data_file> <num_iterations>`

`build/bin/gs_serial <data_file> <num_iterations> [<num_threads (default 4)> [<tile_size (default 16)>]]`

using the serial Gauss-Seidel as an example

## Running tests

You can run the tests we provide by executing one of the programs
* `build/bin/part1_tests`
* `build/bin/part2_tests`
* `build/bin/combined_tests`

You can also run the tests by typing `make test` from the build directory, however, that provides less informative output for failed tests.
Try the "--help" option to see various options.

# Running benchmarks

Run benchmarks by executing one of the programs
`build/bin/part1_bench`
`build/bin/part2_bench`
`build/bin/combined_bench`

Try the "--help" option to see various options.

## Part2 Problem files

The files in the `data` directory contain problem descriptions.
These files start with a line
`SIZE: <number_of_rows> <number_of_cols>`

followed by several lines

`BOUND: <start_row> <start_col> <end_row_inclusive> <end_col_inclusive> <value_to_fix_to>`

You can use these to debug and test your program, make movies, etc. if you like. You will not need them for the minimum version of this project.
# Gauss-Seidel-Open-MP
