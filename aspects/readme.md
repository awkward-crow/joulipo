# aspects

An aspect-oriented style where profiling is applied transparently to existing functions without modifying them. The same interface is exported whether or not profiling is active.

## `tf-x.jl`

The multi-file version. `TF.jl` provides the core functions; `A.jl` wraps each one with a profiler and re-exports them under the same names. The caller (`tf-x.jl`) is unaware of the difference — swap `using A` for `using TF` to run without profiling.

Run with `JULIA_LOAD_PATH` set so the modules can be found:

```sh
JULIA_LOAD_PATH="$JULIA_LOAD_PATH:$(pwd)" ./tf-x.jl ../pride-and-prejudice.txt
```

The `import ... as` syntax in `A.jl` is what makes this work cleanly:

```julia
import TF: extract_words as extract_words_raw
```

The original function is imported under a temporary name, leaving the public name free for the profiled version.

## `tf.jl`

The same approach in a single file.

## `tf-b.jl`

An alternative implementation using `setglobal!` to wrap functions after definition, closer to the Python original. This requires functions to be defined with anonymous syntax:

```julia
extract_words = function(path_to_file) ... end
```

The standard `function extract_words(...) end` form leads to `extract_words` being treated as a constant and attempting to reassign it will give an error.
