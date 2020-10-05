## Secure Shell Remote Management

An SSH addon like the core [Terminal & SSH](https://github.com/home-assistant/hassio-addons/tree/master/ssh) and the community [SSH & Web Terminal](https://github.com/hassio-addons/addon-ssh) addons, but optimised for remote management.

## Why do this?

To remotely manage your home assistant box, using popular Continuous Integration (CI), infrastructure as code, automation, configuration management techniques. The ethos is to treat your home assistant machine as [cattle, not a pet](https://www.google.com/search?q=cattel+vs+pet).

## What kind of remote management?

Running `ssh`, `git` or `ansible` commands on your home assistant machine, from a remote machine. Here are some examples. None of these work easily with the other addons (to my knowledge).

e.g. run an `ssh` command, like this:
```bash
ssh hassio@homeassistant.local "ha info"
```

e.g. run a `git` command, like this.:
```bash
git clone --origin homeassistant git@homeassistant.local:config
# make some updates...
git add .
git commit -m "updates something"
git push homeassistant master

```

e.g. run an `ansible` command, like this.:
```bash
ansible homeassistant -m ping
ansible homeassistant -m raw -a "ha info"
```

## Licence

Apache License Version 2.0

See [here](../LICENSE).

## Contributors

Adam Griffiths
