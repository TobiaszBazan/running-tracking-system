# running-tracking-system

Running Tracking System is a college databases project focused on schema design, data generation, and SQL benchmark comparisons.

## Repository structure

- `sql/schema/` - schema and setup SQL scripts
- `sql/benchmarks/` - benchmark SQL scripts to execute
- `sql/maintenance/` - maintenance SQL scripts (for example index cleanup)
- `sql/data/` - data loading scripts and generated SQL data
- `sql/results/` - benchmark output artifacts (`.txt`, result snapshots)
- `scripts/` - utility scripts (for example SQL data generation)
- `docs/reports/pdf/` - exported report documents
- `docs/reports/source/` - editable report source files

## Where to find key files

- Main schema: `sql/schema/schema.sql`
- Benchmark scripts: `sql/benchmarks/`
- Benchmark outputs: `sql/results/`
- Reports: `docs/reports/`

## Utility scripts

### `scripts/generate_data.py`

Purpose:
- Generates synthetic SQL inserts for the project tables.

Dependencies:
- Python 3 (standard library only)

Usage from repository root:

```bash
python scripts/generate_data.py
```

Generated file:
- `sql/data/generated_data.sql`

## Repository hygiene rules

1. Use lowercase `snake_case` for new file and directory names.
2. Keep executable SQL scripts in `sql/benchmarks`, `sql/schema`, `sql/maintenance`, or `sql/data` based on purpose.
3. Keep generated outputs only in `sql/results` (do not mix them with executable SQL scripts).
4. Keep automation helpers in `scripts/`.
5. Keep documentation artifacts in `docs/`, with editable sources and exported files separated.
