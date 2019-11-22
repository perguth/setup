# \#setup

📜 Set up ChromeOS and RaspberryPi.

```sh
# Trigger setup by running
# on the installation target device.
curl https://raw.githubusercontent.com/perguth/setup/master/README.md | sudo sh
```

## API

```sh
setup user@target
# Be fast and repeatable!
# Update if already set up!
```

- [ ] All user promts before blocking [system calls](https://www.google.com/search?q=node+exec+or+spawn&rlz=1CAVNXA_enDE874&oq=node+exec+or+spawn&aqs=chrome..69i57j0l5.4637j0j7&sourceid=chrome&ie=UTF-8).
- [ ] Sane `-y`/`--yes` option. Else a `Choose [ YES / no ]` mechanism like provided by `apt`.
- [ ] Summary and relevant information in the end (eg. Ygg address).
- [ ] Use [terminal-menu](https://github.com/substack/terminal-menu) for UI.
- [ ] Run update segments (eg. docker) in async processes but instead of callback or promise use [nanobus](https://github.com/choojs/nanobus).
- [ ] Mutate and persist internal state using a [Choo](https://github.com/choojs/choo/blob/v4.0.0-6/README.md#concepts) like concept:

```sh
 ┌──────────────────┐
 │  Subscriptions  ─┤     User ───┐
 └─ Effects  ◀─────┤             ▼
 ┌─ Reducers ◀─────┴──Actions── DOM ◀┐
 │                                     │
 └▶ Router ─────State ───▶ Views ────┘
 ```
 
 - [ ] Provide standard NPM commands. Use `debug` for loggin use `per-env` and `nodemon`. Surpass `standard`! Yes, you can! 🏖️
 - [ ] Keep code lean, avoid folders and `else`. Keep filesize between ~50 and 500 lines. Scope temporary variables and return often and always 😏 *smirk!*
 - [ ] The internal API should expose `/update` and `/upgrade` calls like `apt` does. Interface definition needs to be followed.

✨ Yep! Use a node REST server to provide a interface to a `ash` shell that then executes Bash.

<sup>[(xo)](https://github.com/perguth/ethical-design-manifesto)</sup>
