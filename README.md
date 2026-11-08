# fsr-diagnose

FortiSOAR appliance troubleshooter. The script is published encrypted; get the key from whoever sent you here.

## Run (on the FortiSOAR box, as csadmin)

```bash
curl -fsSL https://github.com/ftnt-dspille/fsr-diagnose/releases/latest/download/run.sh | sudo env bash
```

It asks for the key, then runs. Options go after `-s --`:

```bash
curl -fsSL https://github.com/ftnt-dspille/fsr-diagnose/releases/latest/download/run.sh | sudo env bash -s -- --fix
```

`--fix` applies no-downtime fixes; `--fix --yes` also applies ones that restart a service. Re-run later with `sudo env bash ~/fsr_diagnose.sh`.
