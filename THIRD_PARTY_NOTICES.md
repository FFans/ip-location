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
- IPv4 XDB SHA-256: `c1d6b65520fb8289e46a05261832481c29cf9d11ef9c2ce817d6a81b20b1f072`
- IPv6 XDB SHA-256: `939f6b46bd2b8bec3cf7c5ceb8ba782266ae9b1f35b5ba7916700dec0b7506ed`

#### IPv4 custom corrections

The IPv4 source data currently has 352 local correction ranges applied with
the official `xdb_maker edit` and `xdb_maker gen` commands from ip2region
`v3.18.0`. The corrections cover 250,350 addresses whose base XDB country code
disagreed with Cogent's public RFC 8805 geofeed. Existing ISP values are
preserved.

Correction batches:

- Batch 1 (`2026-09-09`): 134 ranges and 197,376 addresses identified as
  United States within `154.0.0.0/8`.
- Batch 2 (`2026-09-10`): 52 ranges and 46,896 addresses within
  `154.0.0.0/12`; this adds the remaining non-US country-code corrections for
  that batch range.
- Batch 3 (`2026-09-10`): 48 ranges and 786 addresses within
  `154.18.0.0/18`.
- Batch 4 (`2026-09-10`): 118 ranges and 5,292 addresses within
  `154.18.64.0/18`.
- Correction source: `resources/database/ip2region_v4_corrections.txt`
- Evidence: Cogent public RFC 8805 geofeed
  <https://geofeed.cogentco.com/geofeed.csv>
- Batch 1 geofeed SHA-256:
  `4dbe8623b4192d6256cd4859a9ab31f44e698d84cd32ebd2ddd796d6427b67df`
- Batch 2 geofeed SHA-256:
  `7177ca39d100ec16e7ed1160da153a1da2cf75141a082d428d6b874fe226437f`
- Batch 3 geofeed SHA-256:
  `57c19a3f31a148a166eb3b194acf6b135bef7ecbac81a4b88994e4f1df3e50ea`
- Batch 4 uses the same geofeed snapshot as Batch 3.

ip2region license: Apache License 2.0

The upstream license is reproduced at `lib/ip2region/LICENSE.md`.
