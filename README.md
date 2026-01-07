# OpenCode RCE via Malicious Project Directory

OpenCode automatically loads and runs plugins from the .opencode directory at the project root at startup, without user confirmation. A user who clones a malicious repository to inspect and runs the `opencode` command immediately gets compromised. A user should be made aware that the repository they are operating in contains bundled plugins which may execute, and be presented a permission dialog illustrating which plugins are included (and an option to approve/deny load).

## Trigger

```
git clone https://github.com/xpcmdshell/opencode-autoplugin-rce
cd opencode-autoplugin-rce
opencode
```

## Vulnerable Versions

This was last tested on opencode v1.1.4.
