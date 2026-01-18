# SQL Scripts Toolbox

This repo contains my production-tested SQL Server scripts organized by topic and purpose:
- Collect / Analyze / Fix / Build / Runbooks
- Query Store, Performance diagnostics, XEvents, AOAG, WSFC, Backups, Security

## Naming convention
**Pattern:**
`<AreaCode>-<Topic>-<Action>-<Detail>__<Tag>.sql`

Examples:
- `PERF-Waits-Collect__SAFE.sql`
- `QS-TopRegressions-Analyze__SAFE.sql`
- `AOAG-ReplicaHealth-Collect__SAFE.sql`
- `XE-Create-DeadlocksSession__CHANGE.sql`

## Tags
- `__SAFE` = read-only (safe for prod)
- `__CHANGE` = makes changes (DDL/config)
- `__IMPACT` = can cause noticeable load
- `__PRODOK` = used in production successfully
- `__WIP` = work in progress

## Folder structure
Each area typically has:
- `01_Collect` → gather data fast
- `02_Analyze` → interpret / rank problems
- `03_Fix` or `03_Change` → mitigation steps
- `99_Notes` → docs, links, explanations

## Workflow under pressure
1. Go to the topic folder (Performance / AOAG / QS)
2. Run something from `01_Collect`
3. Use `02_Analyze`
4. Only then run something from `03_Fix` / `03_Change`
