## Notes on CPU compatibility

List of the required features. Note: `wide support`/AMD64 means *both* AMD and Intel.

Greentea OS targets CPUs **at least** from 2012 (Q3 2011 and newer)

- `UEFI` is common since late 2011
- `SSE2` is mandatory on AMD64
- `NX` bit should be present on all AMD64
- `SSE3` wide support since 2005
- `CMPXCHG16B` wide support since 2006
- `PrefetchW` wide support since 2006
- `LAHF/SAHF` wide support since 2005
- `POPCNT` wide support since 2008
- `2 MB` huge pages seems to be mandatory on AMD64
- `I/O APIC` mandatory on multi-core AMD64
- `ACPI 2.0` required by Tofita
- `SSE4.1` wide support since 2011 (CPU with SSE4.1 will have SSE3 and SSSE3)
- `SSSE3` wide support since 2011
- `SSE4.2` wide support since 2011

Virtual machine (like VT-x) extensions may become required in the future.

Emulated features:

- Greentea is supposed to emulate AVX and other features on the older CPUs to allow unsupported apps to run

Optional features:

- `1 GB` huge pages (aka `PDPE1GB`) wide support since 2012 and used as optimization
	- May be not present on virtual machines
- `x2APIC` is optional on AMD and **used** by Greentea if present

Not required features:

**Not** used by Greentea system itself but available for third-party apps.

- `SSE4a` seems like AMD-only
- `AVX` wide support since 2011 (except Atom, some modern Pentium & Celeron, old Xeon)
- `AVX2` introduced in 2013
- `AVX-512` introduced in 2016
