# setup

📜 Set up ChromeOS and RaspberryPi.

```sh
# Trigger setup by running
# on the installation target device.
curl https://raw.githubusercontent.com/perguth/setup/master/README.md | sudo sh
```

## API

```sh
setup user@target
```

- All questions before blocking calls.
- Summary and relevant information in the end.
- Use [terminal-menu](https://github.com/substack/terminal-menu) for UI.
- Run update segments (eg. docker) in async processes but instead of callback or promise use [nanobus](https://github.com/choojs/nanobus).
- Mutate and persist internal state using a [Choo](https://github.com/choojs/choo/blob/v4.0.0-6/README.md#concepts) like concept:

```sh
 ┌──────────────────┐
 │  Subscriptions  ─┤     User ───┐
 └─ Effects  ◀─────┤             ▼
 ┌─ Reducers ◀─────┴──Actions── DOM ◀┐
 │                                     │
 └▶ Router ─────State ───▶ Views ────┘
 ```
 
 - In JS use `debug`, `nanobus`, `standard`, `nodemon`, `fs.exec` or `fs.spawn`.
 - Keep code lean, avoid folders and `else`. Keep filesize between ~50 and 500 lines. Scope temporary variables and return often and always 😏 *smirk*
 - The internal API should expose `/update` and `/upgrade` calls like `apt` does. Interface definition needs to be followed.
 - ✨ Yep! Use a node REST server to provide a interface to a `ash` shell that then executes Bash.

<sup>[(xo)](https://github.com/perguth/ethical-design-manifesto)</sup>
