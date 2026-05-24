# bulletin-board

An event-driven style using a shared mutable dictionary as a bulletin board. Functions communicate by reading from and writing to named slots in a shared `Dict` rather than passing arguments directly.

See `closed-maps` for a related style using prototype-based objects.
