# fsr-diagnose

Encrypted release of `fsr_diagnose.sh`, a read-only FortiSOAR appliance troubleshooter (with optional targeted fixes). The script is AES-256 encrypted; the key is shared separately, never stored here.

## Install and run (on the FortiSOAR appliance, as csadmin)

```bash
curl -fsSLO https://github.com/ftnt-dspille/fsr-diagnose/releases/latest/download/fsr_diagnose.sh.enc && \
  openssl enc -d -aes-256-cbc -pbkdf2 -iter 200000 -md sha256 -in fsr_diagnose.sh.enc -out fsr_diagnose.sh && \
  sudo env bash fsr_diagnose.sh
```

`openssl` asks for the key. Add `--fix` to apply no-downtime fixes, `--fix --yes` to also apply service-affecting ones.
