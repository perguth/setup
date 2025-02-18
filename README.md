# [\#setup](https://github.com/topics/tools)

**📜 Set up ChromeOS and RaspberryPi.**

```sh
# Run this on the installation target: 👩‍💻
curl https://raw.githubusercontent.com/perguth/setup/master/README.md | sudo sh
```

## API

```sh
setup user@target
# Be fast and repeatable!
# Update if already set up!
```

 - [ ] Preferably do all user promts before running blocking [system calls](https://www.google.com/search?q=node+exec+or+spawn&rlz=1CAVNXA_enDE874&oq=node+exec+or+spawn&aqs=chrome..69i57j0l5.4637j0j7&sourceid=chrome&ie=UTF-8) to execute eg. [`apt`](http://manpages.ubuntu.com/manpages/xenial/man8/apt.8.html).
 - [ ] Sane `-y`/`--yes` option. Else a `Choose [ YES / no ]` mechanism like provided by [`apt`](http://manpages.ubuntu.com/manpages/xenial/man8/apt.8.html).
 - [ ] Summary and relevant information in the end (eg. Ygg address).
 - [ ] Use [terminal-menu](https://github.com/substack/terminal-menu) for UI.
 - [ ] Run update segments (eg. docker) in async processes but instead of callback or promise use [nanobus](https://github.com/choojs/nanobus).
 - [ ] Mutate and persist internal state using a nanobus.
 - [ ] Provide standard NPM commands. Use the NPM libs `debug`, `per-env` and `nodemon`. Surpass [`standard`](https://github.com/standard/standard)! Yes, you can! 🏖️
 - [ ] Keep code lean, avoid folders and `else`. Keep filesize between ~50 and 500 lines. Scope temporary variables and return often and always 😏 *smirk!*
 - [ ] The internal API should expose `/update` and `/upgrade` calls like `apt` does. Interface definition needs to be followed.
 - [ ] Prefer [nanostack](https://github.com/yoshuawuyts/nanostack), [server-router](https://github.com/yoshuawuyts/server-router) and [Choo](https://github.com/choojs/choo).

✨ Yep! Use a node REST server to provide a interface to a `sh` shell that then executes Bash.

<sup>[(xo)](https://github.com/perguth/ethical-design-manifesto)</sup>
