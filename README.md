# personal-site

Personal CV / business-card site at [usatov.com](https://usatov.com).

Plain `index.html` + `style.css`, no build step. Served by GitHub Pages from this repository's default branch.

## Local preview

Any static server works, e.g.:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

1. Push to `main` of `tuscen/tuscen.github.io`.
2. In repo Settings → Pages: set source to `Deploy from a branch`, branch `main`, folder `/ (root)`.
3. Custom domain `usatov.com` is configured via [`CNAME`](./CNAME); set the DNS record at the registrar:
   - `ALIAS`/`ANAME`/`A` records for apex `usatov.com` pointing to GitHub Pages IPs (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`)
   - or a `CNAME` if `www.usatov.com` is preferred
4. Enable "Enforce HTTPS" once the certificate is issued.
