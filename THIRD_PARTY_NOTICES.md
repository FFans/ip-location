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
- IPv4 XDB SHA-256: `46f7ed9945a333ea5622407d918c8852d7e70a310ed33c465534150d3b619ce9`
- IPv6 XDB SHA-256: `939f6b46bd2b8bec3cf7c5ceb8ba782266ae9b1f35b5ba7916700dec0b7506ed`

#### IPv4 custom corrections

The IPv4 source data currently has 527 local correction ranges applied with
the official `xdb_maker edit` and `xdb_maker gen` commands from ip2region
`v3.18.0`. The corrections cover 391,918 addresses whose base XDB country code
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
- Batch 5 (`2026-09-10`): 20 remaining ranges and 6,960 addresses within
  `154.17.0.0` through `154.19.255.255`.
- Batch 6 (`2026-09-10`): 51 ranges and 66,720 addresses within
  `154.20.0.0` through `154.31.255.255`.
- Batch 7 (`2026-09-10`): 104 ranges and 67,888 addresses within
  `154.32.0.0` through `154.43.255.255`.
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
- Batch 5 uses the same geofeed snapshot as Batch 3.
- Batch 6 uses the same geofeed snapshot as Batch 3.
- Batch 7 uses the same geofeed snapshot as Batch 3.

ip2region license: Apache License 2.0

The upstream license is reproduced at `lib/ip2region/LICENSE.md`.
