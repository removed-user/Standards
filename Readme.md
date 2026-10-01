

#### FHS is not necessarily POSIX

An operating system can techinally be 100% POSIX compliant without following the FHS layout at all
Using only the bare minimum `/dev` and `/tmp` directories. 

But... that's a good recipe for horrible system design.

Realistically.
Both are crucial to Unix-like systems
POSIX focuses on system behaviors and APIs
While FHS focuses on the 
- naming
- organization
- function and
- purpose
of system directories
