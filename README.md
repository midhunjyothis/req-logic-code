# Req → Logic → Code

Mini-MVP to turn business requirements → validated logic → Python → DAX/SQL.

## Why
Make client requirements unambiguous, verify logic fast, and produce code consistently.

## Folder Map
- docs/requirements • raw client inputs
- docs/logic • structured logic (GIVEN–WHEN–THEN)
- docs/validation • sign-off notes & test cases
- src/python • primary analysis code
- exporters/sql • SQL exports
- exporters/dax • DAX exports
- samples/inputs • sample requirement texts
- samples/data • sample CSV/Excel
- tests • minimal checks

## Workflow
1) **Requirement → Logic**: write 3 GIVEN–WHEN–THEN scenarios (incl. 1 edge case) in `docs/logic/`.
2) **Logic → Python**: implement minimal Python in `src/python/` that produces a summary table + metrics.
3) **Validate**: record client confirmation in `docs/validation/`.
4) **Export**: translate Python output to **SQL**/**DAX** in `exporters/`.

## Definition of Done (MVP)
- [ ] 1 real requirement captured in `docs/requirements/`
- [ ] 3 scenarios in `docs/logic/`
- [ ] `src/python/main.py` runs on `samples/data/*`
- [ ] SQL & DAX equivalents produced
- [ ] Validation note added

## Usage (later)
```bash
python src/python/main.py --input samples/data/finance.csv
