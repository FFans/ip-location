# Third-party notices

## ip2region

This extension includes the official PHP XDB query binding and compressed
IPv4/IPv6 XDB database files from
[`lionsoul2014/ip2region`](https://github.com/lionsoul2014/ip2region).

### PHP binding

- Upstream version: `v3.11.2`
- Upstream commit: `f302c68012c55fd8d2d16e6e4fd1716c54a25dfa`
- Source path: `binding/php/xdb/Searcher.class.php`
- Local path: `lib/ip2region/xdb/Searcher.php`

### Database snapshots

- IPv4 base snapshot date: `2026-08-28`
- IPv4 upstream data commit: `7e4c5b6761451c734db51e2b0652219ffc1aba36`
- IPv6 snapshot date: `2026-08-27`
- IPv6 upstream commit: `800d19424237f4be5f2081e6cd9547d98f3871c3`
- Upstream branch: `master`
- Upstream paths: `data/ipv4_source.txt`, `data/ip2region_v4.xdb`, `data/ip2region_v6.xdb`
- Local paths: `resources/database/ip2region_v4.xdb.gz`, `resources/database/ip2region_v6.xdb.gz`
- IPv4 XDB SHA-256: `f0e5fa12f6dc697273192ca90442729a676545c26975339144d520ad9510ea52`
- IPv6 XDB SHA-256: `939f6b46bd2b8bec3cf7c5ceb8ba782266ae9b1f35b5ba7916700dec0b7506ed`

#### IPv4 custom corrections

The IPv4 source data has 134 local correction ranges applied with the official
`xdb_maker edit` and `xdb_maker gen` commands from ip2region `v3.18.0`.
They cover 197,376 addresses in `154.0.0.0/8` that Cogent's public RFC 8805
geofeed identifies as United States while the base XDB country code was not
`US`:

- Affected `/16` blocks: `154.3`, `154.9`, `154.12`, `154.13`, `154.17`,
  `154.18`, `154.19`, `154.21`, `154.22`, `154.28`, `154.29`, `154.43`,
  `154.51`, `154.52`, `154.53`, `154.57`, `154.58`, `154.59`, `154.61`,
  `154.62`, `154.63`, and `154.64`
- Correction source: `resources/database/ip2region_v4_corrections.txt`
- Evidence: Cogent public RFC 8805 geofeed
  <https://geofeed.cogentco.com/geofeed.csv>
- Geofeed snapshot date: `2026-09-09`
- Geofeed snapshot SHA-256:
  `4dbe8623b4192d6256cd4859a9ab31f44e698d84cd32ebd2ddd796d6427b67df`
- Corrections applied: `2026-09-09`

License: Apache License 2.0

The upstream license is reproduced at `lib/ip2region/LICENSE.md`.
