# Dotfiles

Personal dotfiles managed with [yadm](https://yadm.io) (Yet Another Dotfiles Manager).

## Quick Start

### New Machine Setup

```bash
# Install yadm
brew install yadm

# Clone and bootstrap
yadm clone --bootstrap https://github.com/alexfazio/dotfiles.git

# Decrypt secrets (if needed)
yadm decrypt
```

The bootstrap script automatically:
- Detects if this is the primary or secondary machine
- Disables push for secondary machines (pull-only)
- Installs essential tools via Homebrew
- Creates host-specific symlinks

### Check Status

```bash
yadm status
# or use the alias:
dfs
```

## Structure

### Host-Specific Configs (Alternates)

yadm uses file suffixes to provide different configs per machine:

| File | Description |
|------|-------------|
| `.zshrc##default` | Portable base config for all machines |
| `.zshrc##hostname.Alex-MBP` | Overrides for Alex's MacBook Pro |

The appropriate file is symlinked to `.zshrc` based on hostname.

### Key Directories

```
~/.config/
├── aerospace/     # Tiling window manager
├── ghostty/       # Terminal emulator
├── kitty/         # Alternative terminal
├── nvim/          # Neovim config
├── wezterm/       # WezTerm terminal
├── yazi/          # File manager
└── yadm/
    ├── bootstrap  # New machine setup script
    ├── encrypt    # Patterns for encrypted files
    └── gitignore  # Files to never track
```

## Primary vs Secondary Machines

| Machine Type | Can Push | Can Pull |
|-------------|----------|----------|
| Primary (Alex-MBP) | Yes | Yes |
| Secondary (others) | No | Yes |

Secondary machines are configured as pull-only to prevent accidental overwrites from test machines or temporary setups.

To enable push on a secondary machine:
```bash
yadm remote set-url --push origin git@github.com:alexfazio/dotfiles.git
```

## Secrets Management

Sensitive files are encrypted with GPG and stored in the repo:

```bash
# Encrypt secrets (primary machine only)
yadm encrypt

# Add encrypted archive to git
yadm add ~/.local/share/yadm/archive
yadm commit -m "Update encrypted secrets"
yadm push

# Decrypt on new machine
yadm decrypt
```

### Encrypted Files

Patterns in `~/.config/yadm/encrypt`:
- `.secrets.env` - Environment secrets
- `.ssh/id_*` - SSH private keys (not public keys)
- `.gnupg/private-keys-v1.d/*` - GPG private keys
- `.config/gh/hosts.yml` - GitHub CLI auth

## Daily Usage

```bash
# Check what changed
yadm diff

# Add and commit changes
yadm add -u
yadm commit -m "Update configs"
yadm push

# Pull latest from remote
yadm pull
```

## Requirements

- macOS (tested on Sonoma)
- Homebrew
- GPG (for secrets decryption)

## License

MIT
