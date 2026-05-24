# data-spaces

A concurrent style where tasks communicate by passing values through shared channels rather than sharing memory directly. `tf.jl` uses tasks; `tf-t.jl` uses threads.

```sh
julia --threads 5 tf.jl ../pride-and-prejudice.txt
```
