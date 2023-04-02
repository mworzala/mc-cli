# mc-cli
todo write more here


## Command Spec
`<>` indicates required arg
`[]` indicates optional arg
otherwise it is a literal string

### Account management

- `mc account default|use` - Show the current default account
- `mc account default|use <username|uuid>` - Set the default account
- `mc account login` - Login to a new account with Microsoft
- ! `mc account list` - Show a list of all known accounts

### Java management

- `mc java default|use` - Show the current default java installation to be used
- `mc java default|use <name>` - Set the default installation
- ! `mc java list` - List all discovered java installations
- ! `mc java add <path-to-exe> [name]` - Discover a new java installation with the given path, optionally with the given name. If the name is not specified, one will be generated.
- !! `mc java install <version> [name]` - Install a new java dedicated to Minecraft

### Profile management

- `mc install <mc-version> [name]` - Install vanilla minecraft (profile will be named as version if unspecified)
- `mc install <mc-version> [name] --fabric [loader-version]` - Install fabric, todo can a string arg have an optional value?
- `mc run <profile>` - Launch a profile immediately

### Config management
maybe

## Configuration

All subject to change, none of it is implemented

```
# Autolink options describe whether to symlink those resources between different instances
# todo is this really viable?
autolink.config = bool
autolink.servers = bool
autolink.saves = bool
autolink.resourcepacks = bool
```