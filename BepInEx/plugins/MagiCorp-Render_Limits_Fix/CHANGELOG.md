## 1.16.0
- Rebuilt and validated against Valheim 1.0.14 / network version 40.
- Fixed a server range-limit bypass where an excessive loaded radius could exceed Maximum generated zones.
- Added bounded force-active client payloads (default maximum 256 zones) and malformed RPC handling.
- Invalid force-active config coordinates are ignored instead of silently activating zone 0,0.
- Keeps the original `render_limits` plugin GUID and configuration compatibility.

## 1.15.1
- Valheim 1.0.12 compatibility port.
- Fixed startup `Terminal.ConsoleCommand` MissingMethodException.
- Ported zone and simulation-distance APIs introduced by Valheim 1.0.12.
- Updated forced-sector object lookup for the current ZDO API.
