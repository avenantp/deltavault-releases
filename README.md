# DeltaVault Releases

Signed, downloadable builds of DeltaVault's on-premises tools. The product source lives in a private repository; this repository exists so customers can fetch installers directly.

## What ships here

| Tag pattern | Artifact | Platforms |
| --- | --- | --- |
| `agent-vX.Y.Z` | DeltaVault Local Agent (`dv-agent`) | Windows `.msi`, macOS `.pkg` (Apple Silicon + Intel), Linux `.deb` / `.rpm` |
| `cli-vX.Y.Z` | Verify Connection CLI (`dv-verify`) | Windows `.exe` (self-contained, no runtime install) |

## Verifying a download

- **Windows:** installers and executables are Authenticode-signed by **DELTAVAULT PTY LTD** (SSL.com EV). Check with `Get-AuthenticodeSignature <file>` - the status must be `Valid`.
- **macOS:** packages are Developer ID-signed and notarized. Check with `spctl --assess --type install <file>.pkg`.
- **Linux:** `.deb` / `.rpm` ship with detached GPG signatures (`.sig`). Public key: https://www.deltavault.ai/.well-known/release-pubkey.asc

More at https://www.deltavault.ai