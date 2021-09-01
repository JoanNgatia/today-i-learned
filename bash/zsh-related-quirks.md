## zsh related quirks

### Context

I currently use `zsh` as my shell environment. Overtime, I have noticed that not all commands translate as well for both `bash` and `zsh` environments.

Here's some cases where I found that to be the case.

- When running a pip install for a specific section/sub-section of a library,
    e.g. `pip install requests[security]`, we get the error: `zsh: no matches found: requests[security]`.

    Well, turns out `zsh` uses square brackets for pattern matching. This means that if you pass literal square brackets as an arg to a command, they will need to be escaped.

    This is done by adding quotes around the argument: `pip install 'requests[security]'`

    One [SO user](https://stackoverflow.com/a/30539963) suggests possibly disabling this pattern matching for pip on zsh by adding this to the `~/.zshrc`.

    `alias pip='noglob pip'`
