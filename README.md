## Notes

- These files are Bird 1.x compatible:
  - [bird_roa_dn42.conf](bird_roa_dn42.conf)
  - [bird4_roa_dn42.conf](bird4_roa_dn42.conf)
  - [bird6_roa_dn42.conf](bird6_roa_dn42.conf)
- These files are Bird 2.x compatible:
  - [bird_route_dn42.conf](bird_route_dn42.conf)
  - [bird4_route_dn42.conf](bird4_route_dn42.conf)
  - [bird6_route_dn42.conf](bird6_route_dn42.conf)
- These files are [Routinator][2] and [gortr][3] ([src][6]) compatible:
  - [export_rfc8416_dn42.json](export_rfc8416_dn42.json) _(SLURM standard, format specified in [RFC 8416][4])_
- These files are [gortr][3] compatible:
  - [export_dn42.json](export_dn42.json)

Note the gortr source file is DateTime stamped only, it is not signed with any certificaty. So you will need to add
`-verify=false` as a runtime parameter when loading the cache file. Alternatively, use gortr with a slurm file
instead (e.g. `-slurm export_rfc8416_dn42.json`) as a command-line parameter.

## [Last merge commit][0] at [dn42 registry][1]

```
Commit e7f248064bc6a084c0ce7f1f323266324299e380
Merge: fbf438494 cb73b4d6b
Date:   2021-06-06 17:19:00 +0000

    Merge pull request 'Register domain names' (#864) from crewmate-20210605/domain-name into master
```

## crontab

You can setup a [cronjob][5] to check in with updates to the ROA files listed
above on regular intervals.

Currently the ROA files published here is refreshed every 10th hour if
updates has been made to the [DN42 registry][1].

## Misc statistics

- ROAs IPv4:  1519
- ROAs IPv6:  1310
- ROAs total: 2829

[0]: https://git.dn42.dev/dn42/registry/commit/e7f248064bc6a084c0ce7f1f323266324299e380
[1]: https://git.dn42.dev/dn42/registry
[2]: https://github.com/NLnetLabs/routinator
[3]: https://github.com/cloudflare/gortr
[4]: https://tools.ietf.org/html/rfc8416
[5]: doc/crontab.md
[6]: https://github.com/cloudflare/gortr/#configure-filters-and-overrides-slurm

