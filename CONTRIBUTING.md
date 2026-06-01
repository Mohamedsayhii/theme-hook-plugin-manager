# Contributing

Thanks for improving Theme Hook Plugin Manager.

The project is intentionally small: shell scripts, app plugins, and user-facing docs.

## Good Contributions

- New app plugins
- Fixes for existing app plugins
- Better setup or troubleshooting documentation
- Compatibility updates for current Omaniri themes
- Small CLI improvements that keep `thpm` simple

## Plugin Contributions

Keep plugins focused on one app or one integration. Put new bundled plugins in:

```text
theme-set.d/
```

Use a numeric filename prefix, such as:

```text
40-myapp.sh
```

Add the app to the README's supported app list. If the plugin needs special user setup, add a short note to the README troubleshooting section.

For the plugin API and example script, see [docs/plugins.md](docs/plugins.md).

## Validation

Before opening a pull request, run the test suite:

```bash
tests/run.sh
```

If you can test on Omaniri, also run:

```bash
thpm run
```

or:

```bash
omaniri-hook theme-set
```

## Project Notes

Theme colors come from:

```text
~/.config/omaniri/current/theme/colors.toml
```

Do not add new integrations that read generated terminal theme files as the source of truth.

User-facing language should use "plugin" rather than older hook-specific terms.

## Credits

This project is based on [imbypass/omaniri-theme-hook](https://github.com/imbypass/omaniri-theme-hook). Keep attribution intact when reusing or adapting existing plugin work.
