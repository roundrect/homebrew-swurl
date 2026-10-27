# Homebrew tap for Swurl

[Swurl](https://roundrect.download/swurl) is a link router for macOS. It becomes your default browser and opens
every link you click in the browser and profile your rules choose, with a menu bar app and a `swurl` command.

```sh
brew install --cask roundrect/swurl/swurl
```

**Not released yet.** The cask is added here with Swurl's first release; until then the command above finds
nothing.

Requires macOS 15 (Sequoia) or later. The cask installs `Swurl.app` and links the `swurl` command-line tool.

## Releasing a new version

In the Swurl repository: `NOTARY_PROFILE=<profile> make release VERSION=x.y.z`, attach `dist/Swurl-x.y.z.dmg` and
`dist/appcast.xml` to GitHub release `vx.y.z` on roundrect/swurl, then update `version` and `sha256` in
`Casks/swurl.rb` here (or `brew bump-cask-pr --version x.y.z roundrect/swurl/swurl`).
