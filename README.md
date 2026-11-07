# Acratic Professional Services website

## What this is

The one-page static website for Acratic Professional Services, the trading name of Hacker Bear PTY LTD for its cyber security business. It is plain HTML5 and CSS3 with no JavaScript, built for GitHub Pages at https://acratic.com.au/.

## Publishing

- GitHub Pages publishes from the main branch root.
- Set the custom domain to acratic.com.au in the repo under Settings > Pages.
- Tick Enforce HTTPS once it becomes available. GitHub says this can take up to 24 hours.

## DNS records

Verified against GitHub's Pages documentation on 2026-11-07.

| Record | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | pwnagebybutchy.github.io |

The CNAME target is the GitHub account that owns the repo. Update it if the repo is transferred to an organisation.

GitHub recommends verifying the domain in your GitHub settings before adding it to the repo, to prevent domain takeover. The existing A records pointing at the home IP must be removed.

## Check

```bash
dig acratic.com.au +noall +answer -t A
dig www.acratic.com.au +noall +answer -t CNAME
```

## Owner steps

1. Create the GitHub repo.
2. Push the main branch.
3. Set the custom domain to acratic.com.au in Settings > Pages.
4. Set the DNS records above.
5. Remove the old A records pointing at the home IP.
6. Enforce HTTPS once GitHub allows it.
7. The ACN in the index.html footer is 698 215 664.

---

*© Acratic Professional Services. All rights reserved.*
