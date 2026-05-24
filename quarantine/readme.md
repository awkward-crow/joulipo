# quarantine

A monadic style that isolates I/O by wrapping impure operations in a `Quarantine` container. Pure functions are chained onto it with `bind!` and nothing executes until `execute` is called.
