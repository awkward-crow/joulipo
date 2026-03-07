# data spaces

## tasks and threads

File `tf.jl` uses tasks while `tf-t.jl` makes use of threads.

## usage

See usage comment it `tf-t.jl`,

```sh
julia --threads 5 tf-t.jl ../pride-and-prejudice.txt
```

## performance

Messing around with hyperfine shows no advantage to using threads, if anything it may be a little slower! Too much overhead, too little computation?


### end
