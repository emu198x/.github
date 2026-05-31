# Security policy

Emu198x runs untrusted media — ROMs, disk images, tapes, snapshots — so the
realistic risks are crashes, hangs, or runaway memory when it's fed malformed or
hostile input, rather than remote compromise. Reports are welcome all the same.

## Reporting

Please report suspected vulnerabilities privately to **steve@stevehill.xyz**
rather than opening a public issue. Include the input (or a way to obtain it)
and the steps to reproduce.

This is a small project without a formal response window, but reports are read
and acted on. Credit is given gladly once a fix ships, unless you'd rather stay
anonymous.

## Scope

In scope: the emulator mishandling untrusted media (crashes, hangs, memory
blow-up) or the scripting/MCP surface doing something it shouldn't. Out of
scope: issues in dependencies better reported upstream, and theoretical concerns
without a reproduction.
