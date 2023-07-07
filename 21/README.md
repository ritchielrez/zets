# How to get volume from `pactl`

Run this command:
```bash
pactl list sinks | grep "^[[:space:]]Volume:"
```

Here, `^` tells `grep` to match characters start of a line. Inside `[]`, `[:space:]` refers to a **character class**,
indicating a *space*. So the `grep` command searches for a line, starting `Volume:` string following a *space*.

To get the **volume percentage** only, run this:
```bash
pactl list sinks | grep "^[[:space:]]Volume:" | awk '{print $5}'
```

`awk` command helps us to filter out the 5th field from the piped output, containing the **volume percentage**.
