# cal.diy-image

Builds [calcom/cal.diy](https://github.com/calcom/cal.diy) (MIT) from source on GitHub Actions and
publishes `ghcr.io/haydenw22/cal.diy`. Upstream ships no prebuilt image, and the build is too heavy
for the home server's Docker vdisk.

**Update the image:** Actions → *Build Cal.diy image* → *Run workflow* (defaults build upstream `main`
for `https://book.whittledigitalsolutions.com`). Then on the server:

```bash
cd /mnt/user/appdata/calcom && docker compose pull && docker compose up -d
```

Tags: `latest` plus `YYYYMMDD-<upstream sha>` for rollbacks. No secrets live in this repo or the image.
