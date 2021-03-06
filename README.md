# zsh yarn completions
> Yarn completions for Z-shell that supports `yarn workspaces`

## What is does?
- completes for all yarn commands and subcommands
- completes default flags
- `add` recommends packages from cache
- `remove` | `upgrade` | `upgrade-interactive` recommends packages from *package.json*
- support `global` completion
- support workspaces


## Requirements:
  - [zsh](https://github.com/zsh-users/zsh) - `Z-shell`

## Installation

### Using [Antigen](https://github.com/zsh-users/antigen)
```
antigen bundle chrisands/zsh-yarn-completions
```

### Using [zplug](https://github.com/zplug/zplug)
```
zplug "chrisands/zsh-yarn-completions", defer:2
```

### Using [Oh My Zsh!](https://github.com/robbyrussell/oh-my-zsh) as custom plugin
Clone zsh-yarn-completion into your custom plugins repo
```
git clone https://github.com/chrisands/zsh-yarn-completions ~/.oh-my-zsh/custom/plugins/zsh-yarn-completions
```
Then load as a plugin in your .zshrc
```
plugins+=(zsh-yarn-completions)
```

### Manually
Clone this repository somewhere (~/.zsh-yarn-completion for example)
```
git clone https://github.com/chrisands/zsh-yarn-completions.git ~/.zsh-yarn-completions
```
Then source it in your .zshrc
```
source ~/.zsh-yarn-completions/zsh-yarn-completions.plugin.zsh
```

### Aliases
| Alias | Command                |
| ----- | ---------------------- |
| `y`   | `yarn`                 |
| `yi`  | `yarn install`         |
| `ya`  | `yarn add`             |
| `yad` | `yarn add -D`          |
| `yga` | `yarn global add`      |
| `yr`  | `yarn remove`          |
| `ygr` | `yarn global remove`   |
| `yl`  | `yarn link`            |
| `yu`  | `yarn unlink`          |
| `yw`  | `yarn workspace`       |
| `ywi` | `yarn workspaces info` |

## Roadmap
- [ ] suggest unique flags for different commands
- [ ] `config` `set` | `get` suggest config keys (?)
- [ ] `add` find faster way to fetch from cache
- [x] replace `jq` with native tools
- [x] add error validation
- [x] add aliases

## Contribution
Any contribution are welcome!
## License
[MIT](/LICENSE)

## Acknowledgments
[zsh-better-npm-completion](https://github.com/lukechilds/zsh-better-npm-completion) — used few function from project and helped understand how to write proper autocompletion system for zsh.
