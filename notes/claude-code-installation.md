# Claude Code installation investigation

## Goal
Attempt to download and inspect the `@anthropic-ai/claude-code` npm package (or official install script) so we can study the CLI entry points, command definitions, configuration assets, module graph, and behavior for future parity work.

## Attempted acquisition paths
- **npm registry**: `npm pack @anthropic-ai/claude-code` and `npm view @anthropic-ai/claude-code dist.tarball` both failed with HTTP 403 errors before any package metadata could be retrieved. The registry access is blocked in this environment.
- **Direct install script**: Downloading the official installer via `curl -fsSL https://claude.ai/install.sh` also returned HTTP 403 and no script could be saved for inspection.
- **Unpkg CDN**: Fetching `https://unpkg.com/@anthropic-ai/claude-code/package.json` returned HTTP 403, so the CDN cannot be used as a fallback source.
- **Local cache / preinstalled CLI**: `which claude` confirms no existing Claude Code binary on the PATH, and the repository does not contain a packaged release or `package.json` to pack locally.

## Current status
Because every external download path is blocked by network policy, we could not unpack the npm tarball or run `claude --help` and other smoke tests. Consequently, the module graph, tool registry, permission model, plugin hooks, and telemetry implementations remain unknown in this environment.

## Next steps when network access is available
1. Re-run `npm pack @anthropic-ai/claude-code` (or `npm install -g @anthropic-ai/claude-code`) to obtain the published tarball.
2. Extract the tarball to a clean workspace, enumerate CLI entry points (likely `bin/claude`), and map imported modules to build a module graph.
3. Run `claude --help` plus representative commands to capture baseline behavior and flags.
4. Collect configuration assets (default config, tool registry definitions, plugin schemas, telemetry endpoints) for parity notes in the forthcoming Python port.
