# joulipo -- exercises in programming style in julia

Inspired by the book "Exercises in Programming Style" by Cristina Videira Lopes and based on her [github repo](https://github.com/crista/exercises-in-programming-style).

## latest

 - add thread based implementation in data spaces style alongside task based implementation
 - use symbols rather than strings as keys in messages and dictionaries e.g. closed-maps, bulletin-board
 - add Project.toml
 - get lsp working

## next steps

 - ??

## usage

Try, for example

```sh
cd golf
julia --project=@. -i tf.jl
```

The flag `--project=@.` will search upwards from teh current directory for `Project.toml` or similar.

## activate project

Try `activate .` and then `instantiate` at the pkg prompt, this creates file `Project.toml` and `Manifest.toml` which in turn allows julials to do its thing.

## commit `Manifest.toml`

This project is closer to an application than a library so commit.

### end
