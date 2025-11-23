bb083ee add duplicate detection to triage action
eb0b297 Update README.md to reflect GA
a6091b6 fix: Add nano and vim editors to devcontainer with default editor config
46ca39c fix: pin Claude version in Dockerfile to avoid stale builds
33e37bd Fix devcontainer volume security vulnerability
f91aed5 Improve devcontainer Dockerfile following best practices
9285dfb Addition of check for presence of required commands
8e23e7d fix: Use containerEnv for environment variables in devcontainer.json
66ce673 feat: Add CLAUDE_CODE_VERSION arg to devcontainer Dockerfile
6c7836e feat: Add CLAUDE_CODE_VERSION build arg to devcontainer.json
8b2cbe3 feat: Add Docker DNS protection to firewall script
48ed55b Add GitHub workflow to lock stale issues (#4602)
4fd2c49 Enable log output for lock stale issues workflow (#4698)
6418cac Add GitHub workflow to deduplicate issues and Claude configuration
c904f0f Update .claude/commands/dedupe.md
78e0785 simplify Docker DNS restoration using grep and xargs approach
dde41f6 fix: Handle missing Docker DNS rules gracefully in firewall script
07e6bec Update claude-dedupe-issues.yml
1aaffa4 Update dedupe.md
3d5ef4e Add auto-close functionality for duplicate issues
611956d Convert auto-close duplicates workflow to dry run mode
b7116c7 Extract auto-close duplicates script to TypeScript with Bun
7060992 Update .github/workflows/auto-close-duplicates.yml
eb48a37 Improve auto-close duplicates script pagination and filtering
1cc90e9 Update auto-close-duplicates script to actually close issues
d7aa61e Add script to backfill duplicate comments for old issues
399a7dc Add workflow to backfill duplicate comments
478f63b Fix workflow failure by adding workflow_dispatch trigger
f0042af Replace lock-threads action with GitHub Script (#5330)
1579216 Enable auto-close duplicate issues workflow
5af0b38 Add Statsig event logging to GitHub issue workflows
e054111 Remove timeout-minutes from lock-closed-issues workflow (#5455)
c40c658 Add GitHub workflow logging for issue closure events
0662600 Fix GitHub Actions workflow to properly escape issue titles
04cace9 Consolidate GitHub issue closure events to prevent duplicates
4a04589 Use proper 'duplicate' state_reason for issue closures
370a97d fix: improve duplicate issue number extraction in auto-close script
10a1f7d Improving the robustness of prerequisite checks
01fb7af fix: update auto-close-duplicates workflow permissions to write
eb48d5e fix: improve DNS resolution in firewall script to filter CNAME records
5d0b81a Remove log-issue-events workflow
20ba9a3 feat: update dedupe backfill script to filter by issue number
80ceaca Re-add log-issue-events workflow with security fix
6d79459 fix: ensure firewall rules are re-applied on every DevContainer start
f4e707f Add Discord to README.md
c58a7da add Explicit REJECT
2b46e47 update to icmp-admin-prohibited
87e1022 Add stale issue management workflows
d820a4d Add issue close event trigger to log-issue-events workflow
5f52517 chore: Update Dockerfile to standardize environment variable assignments for editor
07e1393 feat(devcontainer): add Claude Code extension and VS Code marketplace URLs
c0a28ee Add workflow configuration
5a24422 Update README.md data usage section
e66b150 Update issue notification workflow
1feaffa Update issue templates
156d9e9 feat: update issue-notify to use repository_dispatch
542b57b Update workflow trigger method
3e00a44 Add workflow variable
8fba17c Fix cross-repo workflow trigger mechanism
cd04312 Update workflow
fa55bc6 Fix broken links in issue template configuration
09a0200 Restore dedupe workflows
1abf1a5 Update demo.gif with latest recording
f7ab5c7 feat: Bundle core plugins into claude-code repo
f876b85 feat: Add security-guidance plugin in claude-code repo (#9223)
5cff787 feat: add feature-dev to public marketplace
00f53cb fix: agent model idenitifer names
559db46 feat: add security-guidance plugin to marketplace.json
87a3b33 refactor: Update agent-sdk-dev plugin structure and configuration (#9230)
88d3666 Remove model specification from new-sdk-app command (#9232)
cabd74f docs: Add comprehensive plugin documentation (#9797)
70cb0d1 feat: upgrade GitHub workflows to use Claude Sonnet 4.5
113ea42 Add automated oncall triage workflow
5d0e5cf Add oncall triage slash command for issue management
546f0b4 Add code-review plugin with automated PR review workflow
48a8bfc Add code-review plugin to marketplace.json
10e1d3f Implement a plugin as alternative for deprecated Explanatory output style
5484a86 Increase oncall triage engagement threshold to 50
015808d feat: Add learning-output-style plugin
ba49573 feat: Incorporate explanatory functionality into learning-output-style plugin
128de2a feat: Add explanatory-output-style and learning-output-style plugins to marketplace
1e95326 docs: Update README installation options to match official docs
3af8ef2 fix: use portable shebang in plugin hooks
f09b24c Update installation instructions for Claude Code
2d0fcac Update code-review.md to avoid flagging test failures
62c3cbc feat: Add frontend-design plugin to marketplace
c91a6b6 feat: Add plugin.json metadata for frontend-design plugin
68f90e0 feat: Add ralph-wiggum plugin for iterative self-referential development
59372c0 feat: Add hookify plugin for custom hook rules via markdown
387dc35 feat: Add plugin-dev toolkit for comprehensive plugin development
5a17f57 docs: Update README with skills and hooks sections (#11818)
3148bac Add comprehensive Claude Code history document
