# joulipo

Julia implementations of the programming styles described in *Exercises in Programming Style* by Cristina Videira Lopes ([source](https://github.com/crista/exercises-in-programming-style)).

Each subdirectory contains a self-contained implementation of the term-frequency problem in a distinct style.

## styles

| directory | style |
|---|---|
| `pipeline` | functions arranged as a linear pipeline |
| `things` | object-oriented, objects with methods |
| `kick-forward` | continuation-passing |
| `the-one` | monadic chaining |
| `quarantine` | monadic I/O isolation |
| `infinite-mirror` | recursion |
| `golf` | code golf — minimal, idiomatic Julia |
| `bulletin-board` | event-driven via a shared mutable object |
| `closed-maps` | prototype-based objects using dictionaries |
| `aspects` | aspect-oriented programming |
| `data-spaces` | concurrent tasks and threads sharing a channel |
| `persistent-tables` | relational storage via PostgreSQL |
| `persistent-tables-juliadb` | relational storage via JuliaDB |

## usage

Run any implementation from within its subdirectory, for example:

```sh
cd pipeline
julia --project=@. tf.jl ../pride-and-prejudice.txt
```

Some implementations have additional requirements or flags — see the readme in each subdirectory.
