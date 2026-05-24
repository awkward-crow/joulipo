# persistent-tables

A relational style where word are stored and frequencies calculated in a PostgreSQL database rather than in-memory data structures.

Requires a running PostgreSQL instance:

```sh
PGHOST=localhost PGUSER=postgres PGPASSWORD=1234 ./tf.jl ../pride-and-prejudice.txt
```
