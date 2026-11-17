# Demo scenario — MacDiskLens

[Back to project](../README.md)

1. Choose a folder and the desired display depth.
2. Run a read-only scan.
3. Explore the largest entries in the tree, table or treemap.
4. Read the scan issues before treating the result as complete.
5. Export the report to CSV.

## Read the sample report

Open [sample-scan.csv](../demo/sample-scan.csv). The first section uses the application's report columns:

| Column | Meaning |
| --- | --- |
| `path` | Scanned folder path. |
| `size_bytes` | Discovered size in bytes. |
| `size_human` | Human-readable representation. |
| `incomplete` | Whether that node's result is incomplete. |
| `direct_issue_count` | Issues reported directly for that node. |

The synthetic root contains Documents, Media and an inaccessible Protected folder. Its known 30 GiB total is incomplete. Documents accounts for 10 GiB and Media for 20 GiB; the inaccessible folder has an unknown actual size. Its zero discovered bytes must not be read as proof it is empty.

After a blank line, `permission_or_scan_issues` introduces the issue section. The file intentionally contains two sections, matching the report writer; treat it as a report rather than one rectangular data table.

Paths and values are invented for this showcase. This is not an application-generated real disk scan, and does not establish current runtime behaviour on a Mac.
